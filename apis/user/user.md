### 数据格式
#### userDTO字段信息(@detail只在请求详情是返回;@all管理时才返回,一般不适用)
```json
{
    "id": 14, //id
    "nickName": "昵称", 
    "realName": "高翔", //@detail姓名
    "mobile": "手机号", //@detail
    "email": "邮箱", //@detail
    "password": "123456",//@all,密码,最短6位，最长12位
    "endorserId": 0, //@detail推荐人id
    "status":10,//@all,状态
    "description":"描述",
    "smallIcon": "/public/takefree/222222.jpg", //小图标
    "bigIcon": "/public/takefree/222223.jpg", //大图标
    "gmtCreate": "2017-11-13 11:36:02", //@detail创建时间
    "lastloginTime": "2017-11-20 11:41:41" //@detail最后登录时间
}
```
### 1 新建用户(待定)
* 1 业务描述

    新建用户，手机号唯一性检查

* 2 调用方式

    url地址：https://{domain}/takefree/v1/user

    请求方式：*POST*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
    {
        "nickName": "goodgirl", //必须
        "realName":"", //可选
        "mobile":"18888888888",//必须
        "endorserId":1, //可选
        "password":"123456",//必须
        "mobile": "", //可选
        "email": "", //可选
        "description":""
    }
    ```

* 5 返回消息体
    ```
    {
        "timestamp": 1504077543058,
        "message": "操作成功",
        "result": {
            $userDTO$
        },
        "status": "200000000",
        "info": "操作成功"
    }
    ```
***
### 2 登录
* 1 业务描述
    
    手机号和密码登录

* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/login
    
    请求方式：*POST*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
    {
        "mobile": "", //必须
        "password":"" //必须，md5两次
    }
    ```
* 5 返回参数：
    ```
    {
        "status": "20000000",
        "message": "操作成功",
        "result": {
            "token": "4c67ac3531cf4d07bda4a15d68bf1569",
            "userDTO": {
                $userDTO$
            },
            "loginTime": "2017-11-20 14:19:32"
        }
    }
### 3 退出登录
* 1 业务描述
    
    手机号和密码登录

* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/logout
    
    请求方式：*DELETE*

* 3 输入参数
    
    无

* 4 请求消息体

    无
    
* 5 返回参数：
    ```
    {
        "timestamp": 1504077543058,
         "message": "操作成功",
         "status": "20000000",
         "info": "操作成功"
    }
***
### 4 更新用户（需要登录）
* 1 业务描述
    
    更新用户信息，手机号和密码不能通过本接口修改

* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/user
    
    请求方式：*PUT*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
    {
        "nickName": "", //可选
        "realName":"", //可选
        "description":"" //可选
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
### 5 用户详细信息（需要登录）
* 1 业务描述：
    
    登录用户获取详细信息。

* 2 调用方式：

    url地址：https://{domain}/takefree/v1/user/detail
    
    请求方式：*GET*
    
* 3 输入参数：
    
    无    

* 4 请求消息体：

    无 

* 5 返回参数
    ```
    {
        "timestamp": 1504077543058,
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": {
            $userDTO$
        }
    }
    ```
***
### 6 用户基本信息
* 1 业务描述

    获取用户基本信息

* 2 调用方式

    url地址：https://{domain}/takefree/v1/user/brief/{id}
    
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
        "result": {
            $userDTO$
        }
    }
    ```
***
