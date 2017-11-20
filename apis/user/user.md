#创建用户
## 1. 业务描述：
新增用户，昵称、真实姓名、手机号、邮箱、邀请用户ID、头像、登录密码、个人简介、收货地址

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/userDTO
请求方式：*POST*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|nick_name|String|昵称|是|
|real_name|String|真实姓名|否|
|mobile|String|手机号|是|
|email|String|邮箱|是|
|endorser_id|Number|推荐人id|是|
|password|String|登录密码|是|
|icon|IoStream|用户头像|否|
|description|String|用户简介|否|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "id": 1
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***

#更新用户信息（需要登录）
## 1. 业务描述：
修改用户信息

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/userDTO
请求方式：*PUT* - 修改

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|nick_name|String|昵称|否|
|real_name|String|真实姓名|否|
|email|String|邮箱|否|
|icon|IoStream|用户头像|否|
|description|String|用户简介|否|
从token里取userId

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "user_id": 1000001
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***

#查看用户详情（需要登录）
## 1. 业务描述：
查看用户信息

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/userDTO/detail
请求方式：*GET*

## 3. 输入参数：
无，从token里取userId

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        *userDTO*
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***

#查看用户详情
## 1. 业务描述：
查看用户信息

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/userDTO/brief/{{id}}
请求方式：*GET*

## 3. 输入参数：
无，从uri里取userId

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        *userDTO*
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***
