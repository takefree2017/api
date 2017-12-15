### 数据格式
#### userAddressDTO字段信息
```json
{
    "id": 14, //id
    "userId": "用户id", 
    "userName": "高翔", //姓名
    "phone": "电话号", 
    "provinceId":100000,//"省编码", 
    "cityId":200100, //"市编码"
    "postcode":100100, //右边
    "address":"地址",
    "isDefault":1,//"默认地址",1,"非默认地址",0;
    "gmtCreate": "2017-11-13 11:36:02", //创建时间
    "gmtModified": "2017-11-20 11:41:41" //最后登录时间
}
```
### 1 新增地址（需要登录）
* 1 业务描述

    增加用户地址

* 2 调用方式

    url地址：https://{domain}/takefree/v1/user/address

    请求方式：*POST*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
    {
        "userName": "高翔",
        "phone": "电话号", 
        "provinceId":100000,
        "cityId":200100,
        "postcode":100100, 
        "address":"地址",
        "isDefault":0
    }
    ```
* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "200000000",
        "info": "操作成功",
        "result": {
            {userAddressDTO}
        }
    }
    ```
***
### 2 删除地址（需要登录）
* 1 业务描述

    删除用户地址

* 2 调用方式

    url地址：https://{domain}/takefree/v1/user/address/{id}

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
### 3 按id查询地址
* 1 业务描述

    删除用户地址

* 2 调用方式

    url地址：https://{domain}/takefree/v1/user/address/{id}

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
        "status": "200000000",
        "info": "操作成功",
        "result": {
            {userAddressDTO}
        }
    }
    ```
***

### 4 查询地址(需要登录)
* 1 业务描述

    删除用户地址

* 2 调用方式

    url地址：https://{domain}/takefree/v1/user/address

    请求方式：*GET*

* 3 输入参数
    
    isDefault=1 //是否默认地址，可选

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
            "result": [{userAddressDTO}...]
        }
    }
    ```
***
### 5 修改地址（需要登录）
* 1 业务描述

    增加用户地址

* 2 调用方式

    url地址：https://{domain}/takefree/v1/user/address/{id}

    请求方式：*PUT*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
    {
        "userName": "高翔",
        "phone": "电话号", 
        "provinceId":100000,
        "cityId":200100,
        "postcode":100100, 
        "address":"地址",
        "isDefault":0
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
