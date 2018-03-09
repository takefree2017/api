## 显摆

### show数据格式
```json
{
    "id": 1,
    "orderId": 1, //订单号
    "takeTime": "2017-11-13 11:36:02", //订单时间
    "shareId": 1, //分享id
    "shareTitle": "title", 
    "sharePicHomepage": "分享首页图片",
    "giverId": 1, //分享者id
    "giverNickName": "分享者昵称", 
    "giverSmallIcon": "分享者小图标", 
    "receiverId": 2, //申请人id
    "receiverNickName": "申请人昵称", 
    "receiverSmallIcon": "申请人小图标", 
    "moodId": 10, //心情id
    "moodName": 1, //心情名称
    "moodIconUrl": 10, //心情图片
    "showContentPreview": "显摆缩略", 
    "content": "显摆内容", 
    "viewCount": 10, //点击量
    "likeCount": 10,//like人数
    "commentCount": 10,//评论次数
    "showPics": [ //图片
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
    "gmtCreate":"2017-11-13 11:36:02", //创建时间
    "gmtCreate":"2017-11-13 11:36:02", //最后修改时间
    "version":1,//版本
    "isCurrentUserLike": true //当前用户是否like
}
```
### 1 创建显摆（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/show

    请求方式：*POST*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
    {
        "orderId": 1, //订单号
        "moodId": 10, //心情id
        "showContentPreview": "显摆缩略", 
        "content": "显摆内容", 
        "showPics": [ //图片
            {
                "picUrl": "/public/takefree/pic/1.jpg", //图片URL
                "sequence":"1" //图片顺序号
            },
            {
                "picUrl": "/public/takefree/pic/2.jpg",
                "sequence":"2"
            },
            {
                "picUrl": "/public/takefree/pic/3.jpg",
                "sequence":"3"
            }
        ]
    }
    ```
* 5 返回消息体
    ```json
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "200000000",
        "info": "操作成功"
        "result": {
            "{show}"
        }
    }
    ```
***
### 2 更新显摆（需要登录）
* 1 业务描述
    
* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/show/{id}
    
    请求方式：*PUT*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
    {
        "orderId": 1, //订单号
        "moodId": 10, //心情id
        "showContentPreview": "显摆缩略", 
        "content": "显摆内容", 
        "showPics": [ //图片
            {
                "picUrl": "/public/takefree/pic/1.jpg", //图片URL
                "sequence":"1" //图片顺序号
            },
            {
                "picUrl": "/public/takefree/pic/2.jpg",
                "sequence":"2"
            },
            {
                "picUrl": "/public/takefree/pic/3.jpg",
                "sequence":"3"
            }
        ]
    }
    ```
* 5 返回参数：
    ```json
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功"
    }
    ```
***
### 3 删除显摆（需要登录）
* 1 业务描述
    
* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/show/{id}
    
    请求方式：*DELETE*

* 3 输入参数
    
    无

* 4 请求消息体

    无
    
* 5 返回参数：
    ```json
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功"
    }
    ```
***
### 4 按id查询显摆
* 1 业务描述
    
* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/show/{id}
    
    请求方式：*GET*

* 3 输入参数
    
    无

* 4 请求消息体

    无
    
* 5 返回参数：
    ```json
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": {
              "{show}"
         }
    }
    ```
***
### 5 查询显摆列表
* 1 业务描述

    显摆列表,时间倒序
    
* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/show
    
    请求方式：*GET*

* 3 输入参数
    
    maxId:可选，最大id(不包含)，用于分页
    
    pageSize:可选，分页数量
    
    pageNo:可选，分页号
    
    shareId:可选，分享id
    
    orderId:可选，订单id
    
    receiverId:可选，获得人id
    
    giverId:可选，分享人id
    
    注意:maxId与pageNo二选一

* 4 请求消息体

    无
    
* 5 返回参数：
    ```json
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": {
              ["{show}"...]
         }
    }
    ```
***
