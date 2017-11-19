### 数据格式
####ShareDTO字段信息(@detail代表只在请求详情是返回)
```json
{
    "id": 1000001,
    "title": "title", 
    "ownerId": 100001, //发布人Id
    "ownerNickName": "发布人昵称",
    "shareDescPreview": "描述缩略",
    "description":"描述",
    "publishTime": "2017-11-14 11:36:02",//发布时间
    "status": "10",//状态。10，草稿；20，发布中；30，已送出；40，取消
    "longitude": 33.33, //@detail,经度
    "latitude": 22.22, //@detail,维度
    "lbsDescription": "地址详情",//@detail
    "viewCount": 10, //点击量
    "commentCount": 10,//回复数量
    "lastCommentViewTime": "2017-11-14 11:36:02",//最后查看回复时间
    "lastCommentTime": "2017-11-13 11:36:02",//最后回复时间
    "applyCount": 10,//申请人数
    "lastApplyViewTime": "2017-11-12 11:36:02", //最后查看申请时间
    "lastApplyTime": "2017-11-13 11:36:02",//最后申请时间
    "likeCount": 10,//like人数
	"picHomepage": "/public/takefree/pic/1.jpg", //首页图片url
	"categories": [//@detail,分类
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
    "sharePics": [ //@detail,图片
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
        "longitude": 33.3333,
        "latitude": 22.2222,
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
        "timestamp": 1504077543058,
        "message": "操作成功",
        "result": {
            "shareId": 1000001
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
            "longitude": 33.3333, 
            "latitude": 22.2222, 
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
* 5 返回参数：
    ```
    {
        "timestamp": 1504077543058,
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功"
    }
    ```
***
### 3 发布分享（需要登录）
* 1 业务描述：
    
    发布分享，包括已有保存草稿(更新兵发布)和新建（新建兵发布）并发布两种情况，已保存草稿则携带id。

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
        "description":"描述", 
        "longitude": 33.3333, 
        "latitude": 22.2222, 
        "lbsDescription": "地址详情",
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
        "timestamp": 1504077543058,
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
        "timestamp": 1504077543058,
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功"
    }
    ```
***
### 5 查看详情
* 1 业务描述

    查看分享详细信息

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
        "timestamp": 1504077543058,
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result":@shareDTO
    }
    ```
***
### 6 查看分享列表
* 1 业务描述

    根据发布人,发布状态查询分享列表

* 2 调用方式

    url地址：https://{domain}/takefree/v1/share
    
    请求方式：*GET*

* 3 输入参数
    
    status:状态,可选
    ownerId:发布人,可选
    maxId:可选，最大id(不包含)，用于分页
    pageSize:可选，分页数量
    pageNo:可选，分页号
    注意:maxId与pageNo二选一
    
* 4 请求消息体
    
    无

* 5 返回消息体
    ```
    {
        "timestamp": 1504077543058,
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        result: [{shareDTO}...]
    }
    ```

***
### 7 用户喜欢的分享列表（需要登录）
* 1 业务描述

    查询用户喜欢的分享列表

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
        "timestamp": 1504077543058,
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        result: [{shareDTO}...]
    }
    ```
***
### 8 用户申请的分享列表（需要登录）//TODO...
* 1 业务描述

    查询用户申请的分享列表

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
        "timestamp": 1504077543058,
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        result: [{shareDTO}...]
    }
    ```
### 9 用户收到的分享列表（需要登录）
* 1 业务描述

    查询用户收到的分享列表

* 2 调用方式

    url地址：https://{domain}/takefree/v1/share/received

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
        "timestamp": 1504077543058,
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        result: [{shareDTO}...]
    }
    ```
