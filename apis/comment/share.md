## 分享评论

### showcomment数据格式
```json
{
    "id": 1,
    "shareId": 1, //分享id
    "userId": 2, //用户id
    "userNickName": "用户昵称", 
    "userSmallIcon": "用户小图标", 
    "content": "评论内容", 
    "parentCommenId": 1,
    "parentUserId": 2, //parent评论用户id
    "parentUserNickName": "parent评论用户昵称", 
    "parentUserSmallIcon": "parent评论用户小图标", 
    "parentContent": "parent评论内容", 
    "parentGmtCreate":"2017-11-13 11:36:02", //parent评论创建时间
    "gmtCreate":"2017-11-13 11:36:02", //创建时间
    "gmtCreate":"2017-11-13 11:36:02", //最后修改时间
    "version":1 //版本
}
```
### 1 创建评论（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/sharecomment

    请求方式：*POST*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
    {
        "shareId": 1,
        "content": "very good",
        "parentCommenId": 2
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
            "{showcomment}"
        }
    }
    ```
***
### 2 删除评论（需要登录）
* 1 业务描述
    
* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/sharecomment/{id}
    
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
### 3 按id查询评论
* 1 业务描述
    
* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/sharecomment/{id}
    
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
              "{sharecomment}"
         }
    }
    ```
***
### 4 查询评论列表
* 1 业务描述

    评论列表,时间倒序
    
* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/sharecomment
    
    请求方式：*GET*

* 3 输入参数
    
    pageSize:可选，分页数量
    
    pageNo:可选，分页号
    
    shareId:可选，分享id

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
              ["{sharecomment}"...]
         }
    }
    ```
***
