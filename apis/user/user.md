### 数据格式
#### userDTO字段信息
```json
{
    "id": 14, //id
    "nickName": "昵称", 
    "realName": "高翔", //姓名
    "mobile": "手机号", 
    "email": "邮箱", 
    "password": "123456",//密码,最短6位，最长12位
    "endorserId": 0, //推荐人id
    "status":10,//状态."未激活",10；"已经激活",20);
    "sex":10,//性别，0,男；1，女
    "birthday":"1997-11-13",//生日
    "description":"描述",
    "smallIcon": "/public/takefree/222222.jpg", //小图标
    "bigIcon": "/public/takefree/222223.jpg", //大图标
    "gmtCreate": "2017-11-13 11:36:02", //创建时间
    "lastloginTime": "2017-11-20 11:41:41", //最后登录时间
    "isFollowee":false //当前用户是否被我like，用于当前用户查看follower
}
```
### 1 新建用户(推荐)（需要登录）
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
        "mobile":"18888888888",//必须
        "description":""
    }
    ```

* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "result": {
            {userDTO}
        },
        "status": "200000000",
        "info": "操作成功"
    }
    ```
***
### 2 密码登录
* 1 业务描述
    
    手机号和密码登录

* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/login/password
    
    请求方式：*POST*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
    {
        "mobile": "", //必须
        "password":"" //必须
    }
    ```
* 5 返回参数：
    ```
    {
        "status": "20000000",
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "result": {
            "token": "4c67ac3531cf4d07bda4a15d68bf1569",
            "userDTO": {
                {userDTO}
            },
            "loginTime": "2017-11-20 14:19:32"
        }
    }
***
### 3 获取登录验证码
* 1 业务描述
    
    手机号和密码登录

* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/login/sms
    
    请求方式：*GET*

* 3 输入参数
    
    mobile //必须

* 4 请求消息体

    无
    
* 5 返回参数：
    ```
    {
        "status": "20000000",
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功"
    }
***
### 4 验证码登录
* 1 业务描述
    
    手机号和密码登录

* 2 调用方式
    
    url地址：https://{domain}/takefree/v1/login/password/sms
    
    请求方式：*POST*

* 3 输入参数
    
    mobile //必须
    
    smsCode //必须

* 4 请求消息体
    ```json
    {
        "mobile": "", //必须
        "password":"" //必须
    }
    ```
* 5 返回参数：
    ```
    {
        "status": "20000000",
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "result": {
            "token": "4c67ac3531cf4d07bda4a15d68bf1569",
            "userDTO": {
                {userDTO}
            },
            "loginTime": "2017-11-20 14:19:32"
        }
    }
***
### 5 退出登录
* 1 业务描述

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
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功"
    }
***
### 6 更新用户（需要登录）
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
        "email": "", //可选
        "smallIcon": "/public/takefree/222222.jpg", //可选
        "bigIcon": "/public/takefree/222223.jpg", //可选
        "description":"" //可选
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
### 7 用户详细信息（需要登录）
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
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": {
            {userDTO}
        }
    }
    ```
***
### 8 用户基本信息
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
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": {
            {userDTO}
        }
    }
    ```
***
### 9 获取关注本人的用户（需要登录）
* 1 业务描述

    获取关注本人的用户

* 2 调用方式

    url地址：https://{domain}/takefree/v1/user/follower
    
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
        "result": [
            {userDTO}...
        ]
    }
    ```
***
### 10 获取本人关注的用户（需要登录）
* 1 业务描述

    获取本人关注的用户

* 2 调用方式

    url地址：https://{domain}/takefree/v1/user/followee
    
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
        "result": [
            {userDTO}...
        ]
    }
    ```
***
