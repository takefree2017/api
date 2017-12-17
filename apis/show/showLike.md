## 关注显摆

### showlike数据格式
```json
{
    "id": 14, //id
    "showId": 1, //显摆id
    "userId": 1, 
    "userNickName": "关注人昵称",
    "userSmallIcon": "/public/takefree/222222.jpg", //发布人小图标
    "gmtCreate":"2017-11-13 11:36:02", //创建时间
    "gmtCreate":"2017-11-13 11:36:02", //最后修改时间
    "version":1 //版本
}
```
### 1 关注显摆（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/showlike

    请求方式：*POST*

* 3 输入参数
    
    showId //必须

* 4 请求消息体
    
    无
    
* 5 返回消息体
    ```json
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "200000000",
        "info": "操作成功",
        "result": {
            {showLike}
        }
    }
    ```
***
### 2 取消显摆关注（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/showlike

    请求方式：*DELETE*

* 3 输入参数

    showId //必须
    
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
### 3 查询显摆关注列表
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/showlike

    请求方式：*GET*

* 3 输入参数
    
    userId 关注人,可选
    
    showId 可选，显摆id
        
    pageSize 可选，分页数量
        
    pageNo 可选，分页号

* 4 请求消息体
    
    无
    
* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "200000000",
        "info": "操作成功",
         "result": [{showlike}...]
    }
    ```
***
