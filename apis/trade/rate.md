## 订单评价

### orderrate数据格式
```json
{
    "id": 1, //id
    "orderId": 1, //分享id
    "rate": 1, //1好评 0差评
    "rateComment": "评价内容", 
    "gmtCreate":"2017-11-13 11:36:02", //创建时间
    "gmtCreate":"2017-11-13 11:36:02", //最后修改时间
    "version":1 //版本
} 
```
### 1 新建评价（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/rate

    请求方式：*POST*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
    {
        "orderId": 1, //分享id
        "rate": 1,
        "rateComment": "评价内容"
    }
    ```

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
### 2 删除评价（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/rate/{id}

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
### 3 修改评价（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/logistics/{id}

    请求方式：*PUT*

* 3 输入参数
    
    无

* 4 请求消息体
    ```
    {
        "rate": 1,
        "rateComment": "评价内容"
    }
    ```
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
### 4 查询评价（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/rate

    请求方式：*GET*

* 3 输入参数
    
    无

* 4 请求消息体
    
    orderId:可选,分享id
    
* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "200000000",
        "info": "操作成功",
        "result": {
             "{rate}"
        }
    }
    ```
***

