#我关注谁
## 1. 业务描述：
用户查看自己关注的好友，支持分页

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/user/{{id}}/followees
请求方式：*GET*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|pageNo|Mumber|当前页码|是|
|pageSize|Mumber|每页尺寸|是|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "userId": 1000001,
        "followees": [
            {
                *user*,
                *address*,
                "isFollower": 1
            },
            {
                *user*,
                *address*,
                "isFollower": 0
            }
        ]
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***

#谁关注我
## 1. 业务描述：
用户查看关注自己的好友，支持分页

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/user/{{id}}/followers
请求方式：*GET*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|pageNo|Mumber|当前页码|是|
|pageSize|Mumber|每页尺寸|是|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "userId": 1000001,
        "followers": [
            {
                *user*,
                *address*,
                "isFollowee": 1
            },
            {
                *user*,
                *address*,
                "isFollowee": 0
            }
        ]
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***