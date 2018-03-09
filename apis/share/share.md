## 分享

### shareDTO数据格式
```json
{
    "id": 1000001,
    "title": "title", 
    "ownerId": 100001, //发布人Id
    "ownerNickName": "发布人昵称",
    "ownerSmallIcon": "/public/takefree/222222.jpg", //发布人小图标
    "shareDescPreview": "描述缩略",
    "description":"描述",
    "publishTime": "2017-11-14 11:36:02",//发布时间
    "status": 10,//状态。10，草稿；20，发布中；30，已送出；40，取消
    "shareModeId":1, //shareMode
    "transferable":1, //是否交接。0,否;1,是
    "transferType":1, //10,物流;20,见面交易;30,支持两种.transferable=1时有效
    "participatory":1, //是否有人参与。0,否;1,是
    "longitude": 33.33, //@detail,经度
    "latitude": 22.22, //@detail,维度
    "lbsDescription": "地址详情",//@detail
    "viewCount": 10, //点击量
    "number": 10,//数量
    "takeNumber": 10,//送出数量
    "commentCount": 10,//评论次数
    "newCommentCount": 5,//最新评论次数
    "applyCount": 10,//申请人数
    "newApplyCount": 3,//最新申请人数
    "likeCount": 10,//like人数
	"picHomepage": "/public/takefree/pic/1.jpg", //首页图片url
	"isCurrentUserLike":true, //当前用户是否like
	"isCurrentUserApply":false, //当前用户是否apply
	"categories": [//分类
        {
            "categoryId": 10001 //分类id
        },
        {
            "categoryId": 10002
        },
        {
            "categoryId": 10003
        }
    ],
    "sharePics": [ //图片
        {
            "picUrl": "/public/takefree/pic/1.jpg", //图片URL
            "sequence":"0" //图片顺序号
        },
        {
            "picUrl": "/public/takefree/pic/2.jpg",
            "sequence":"1"
        },
        {
            "picUrl": "/public/takefree/pic/3.jpg",
            "sequence":"2"
        }
    ],
    "takeOrderDTOS":[ //订单
        {参考订单orderDTO}
    ]
}
```
### 1 创建分享草稿（需要登录）
* 1 业务描述

    用户创建分享，填写标题、描述，选择分享所属类目，上传分享的图片等

* 2 调用方式

    url地址：https://{domain}/takefree/v1/share

    请求方式：*POST*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
    { 
        "title": "title", 
        "description":"描述",
        "number":1,
        "longitude": 33.3333,
        "latitude": 22.2222,
        "shareModeId":1,
        "transferable":1,
        "participatory":1,
        "lbsDescription": "地址详情",
    	"picHomepage": "/public/takefree/pic/1.jpg", 
    	"categories": [
            {
                "categoryId": 10001
            },
            {
                "categoryId": 10002
            },
            {
                "categoryId": 10003
            }
        ],
        "sharePics": [
            {
                "picUrl": "/public/takefree/pic/1.jpg",
                "sequence":"0"
            },
            {
                "picUrl": "/public/takefree/pic/2.jpg",
                "sequence":"1"
            },
            {
                "picUrl": "/public/takefree/pic/3.jpg",
                "sequence":"2"
            }
        ]
    }
    ```

* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "result": {
            "{share}"
        },
        "status": "200000000",
        "info": "操作成功"
    }
    ```
***
### 2 更新分享（需要登录）
* 1 业务描述
    
    修改草稿和已发布分享

* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/share/{id}
    
    请求方式：*PUT*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
        {
            "title": "title", 
            "description":"描述", 
            "number":1,
            "longitude": 33.3333, 
            "latitude": 22.2222, 
            "lbsDescription": "地址详情",
            "shareModeId":1,
            "transferable":1,
            "participatory":1,            
        	"picHomepage": "/public/takefree/pic/1.jpg", 
        	"categories": [
                {
                    "categoryId": 10001 
                },
                {
                    "categoryId": 10002
                },
                {
                    "categoryId": 10003
                }
            ],
            "sharePics": [ 
                {
                    "picUrl": "/public/takefree/pic/1.jpg",
                    "sequence":"0"
                },
                {
                    "picUrl": "/public/takefree/pic/2.jpg",
                    "sequence":"1"
                },
                {
                    "picUrl": "/public/takefree/pic/3.jpg",
                    "sequence":"2"
                }
            ]
        }
    ```
* 5 返回参数：
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功"
    }
    ```
***
### 3 发布分享（需要登录）
* 1 业务描述：
    
    发布分享，包括已有保存草稿(更新并发布)和新建（新建并发布）并发布两种情况，已保存草稿则携带id。

    无论是否已保存草稿，消息体都包含已填写字段。

* 2 调用方式：

    url地址：https://{domain}/takefree/v1/share/publish
    
    请求方式：*POST*
    
* 3 输入参数：
    
    无    

* 4 请求消息体：
    ```json
    {
        "id": 123, //已保存草稿则携带
        "title": "title", //必须
        "number":1,
        "description":"描述", 
        "longitude": 33.3333, 
        "latitude": 22.2222, 
        "lbsDescription": "地址详情",
        "shareModeId":1,
        "transferable":1,
        "participatory":1,
    	"picHomepage": "/public/takefree/pic/1.jpg", //必须,首页图片url
    	"categories": [
            {
                "categoryId": 10001 
            },
            {
                "categoryId": 10002
            },
            {
                "categoryId": 10003
            }
        ],
        "sharePics": [ //必须,图片
            {
                "picUrl": "/public/takefree/pic/1.jpg",
                "sequence":"0"
            },
            {
                "picUrl": "/public/takefree/pic/2.jpg",
                "sequence":"1"
            },
            {
                "picUrl": "/public/takefree/pic/3.jpg",
                "sequence":"2"
            }
        ]
    }
    ```

* 5 返回参数
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功"
    }
    ```
***
### 4 删除分享（需要登录）
* 1 业务描述

    删除分享，后台逻辑删除，草稿和发布中状态的分享可以被逻辑删除，分享主人才能操作

* 2 调用方式

    url地址：https://{domain}/takefree/v1/share/{id}
    
    请求方式：*DELETE*

* 3 输入参数

    无

* 4 请求消息体

    无

* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功"
    }
    ```
***
### 5 查看详情(不需要登录，但是已登录用户需要带上Token)
* 1 业务描述

    查看分享详细信息，如果是发布人则更新最后查看回复及申请时间，否则增加view次数

* 2 调用方式

    url地址：https://{domain}/takefree/v1/share/{{id}}

    请求方式：*GET*

* 3 输入参数
    
    无
    
* 4 请求消息体
    
    无

* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result":@shareDTO
    }
    ```
***
### 6 查看分享列表
* 1 业务描述

    根据条件查询分享列表

* 2 调用方式

    url地址：https://{domain}/takefree/v1/share
    
    请求方式：*GET*

* 3 输入参数
    
    status:状态,可选
    
    ownerId:发布人,可选
    
    maxId:可选，最大id(不包含)，用于分页
    
    pageSize:可选，分页数量
    
    pageNo:可选，分页号
    
    searchWord:可选，在分享title中按关键字搜索
    
    注意:maxId与pageNo二选一
    
* 4 请求消息体
    
    无

* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": [{shareDTO}...]
    }
    ```
***
### 7 用户喜欢的分享列表（需要登录）
* 1 业务描述

    查询用户喜欢的分享列表，可根据发布人筛选

* 2 调用方式

    url地址：https://{domain}/takefree/v1/share/like

    请求方式：*GET*

* 3 输入参数
    
    status:分享状态,可选
    
    ownerId:发布人,可选
    
    pageSize:可选，分页数量
    
    pageNo:可选，分页号
    
* 4 请求消息体
    
    无

* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": [{shareDTO}...]
    }
    ```
***
### 8 用户申请的分享列表（需要登录）
* 1 业务描述

    查询用户申请的分享列表，可根据发布人筛选

* 2 调用方式

    url地址：https://{domain}/takefree/v1/share/apply

    请求方式：*GET*

* 3 输入参数
    
    status:分享状态,可选
    
    ownerId:发布人,可选
    
    pageSize:可选，分页数量
    
    pageNo:可选，分页号
    
* 4 请求消息体
    
    无

* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": [{shareDTO}...]
    }
    ```
***
### 9 用户收到的分享列表（需要登录）
* 1 业务描述

    查询用户收到的分享列表，可根据发布人筛选

* 2 调用方式

    url地址：https://{domain}/takefree/v1/share/takein

    请求方式：*GET*

* 3 输入参数
    
    ownerId:发布人,可选
    
    pageSize:可选，分页数量
    
    pageNo:可选，分页号
    
* 4 请求消息体
    
    无

* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": [{shareDTO}...]
    }
    ```
***
### 10 用户送出的分享列表（需要登录）
* 1 业务描述

    查询用户送出的分享列表，按时间倒序

* 2 调用方式

    url地址：https://{domain}/takefree/v1/share/takeout

    请求方式：*GET*

* 3 输入参数
    
    pageSize:可选，分页数量
    
    pageNo:可选，分页号
    
* 4 请求消息体
    
    无

* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": [{shareDTO}...]
    }
    ```
