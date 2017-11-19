#新增关注人（需要登录）
## 1. 业务描述：
用户查看别人profile后觉得喜欢，新增关注人

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/userDTO/like
请求方式：*POST*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|followeeId|Mumber|被关注人ID|是|
从token里取userId

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "followeeId": 1000001
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***

#取消关注人（需要登录）
## 1. 业务描述：
用户取消曾经关注的人

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/userDTO/like
请求方式：*DELETE*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|followeeId|Mumber|被关注人ID|是|
从token里取userId

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "followeeId": 1000001
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***

#我关注谁（需要登录）
## 1. 业务描述：
用户查看自己关注的好友，支持分页

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/userDTO/followees
请求方式：*GET*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|pageNo|Mumber|当前页码|是|
|pageSize|Mumber|每页尺寸|是|
从token里取userId

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "userId": 1000001,
        "followees": [
            {
                *{userDTO}*,
                *{address}*,
                "isFollower": 1
            },
            {
                *{userDTO}*,
                *{address}*,
                "isFollower": 0
            }
        ]
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***

#谁关注我（需要登录）
## 1. 业务描述：
用户查看关注自己的好友，支持分页

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/userDTO/followers
请求方式：*GET*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|pageNo|Mumber|当前页码|是|
|pageSize|Mumber|每页尺寸|是|
从token里取userId

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "userId": 1000001,
        "followers": [
            {
                *{userDTO}*,
                *{address}*,
                "isFollowee": 1
            },
            {
                *{userDTO}*,
                *{address}*,
                "isFollowee": 0
            }
        ]
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***
