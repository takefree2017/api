## 关注用户

### userLike数据格式
```json
{
    "id": 14, //id
    "userFolloweeId": 1, //被关注人id
    "userFollowerId": 2, //关注人id
    "gmtCreate":"2017-11-13 11:36:02" //"关注时间"
    
}
```
### 1 关注用户（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/userlike

    请求方式：*POST*

* 3 输入参数
    
    folleweeId //必须

* 4 请求消息体
    
    无
    
* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "200000000",
        "info": "操作成功",
        "result": {
            {userLike}
        }
    }
    ```
***
### 2 按id取消关注（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/userlike/{id}

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
        "status": "200000000",
        "info": "操作成功"
    }
    ```
***
### 3 按被关注人id取消关注（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/userlike

    请求方式：*DELETE*

* 3 输入参数
    
    folleweeId //必须

* 4 请求消息体
    
    无
    
* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "200000000",
        "info": "操作成功"
    }
    ```
***
