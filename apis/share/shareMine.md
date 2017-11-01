#用户正在的分享（1）
## 1. 业务描述：
查看用户正在进行的分享，支持分页

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/share/underway
请求方式：*GET*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|pageNo|Number|当前页码|是|
|pageSize|Number|每页尺寸|是|
从token里取userId

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "userId": 1000001,
        "draftCount": 2,
        "shares": [
            {
                *share*
            },
            {
                *share*
            },
            {
                *share*
            },
            {
                *share*
            }
        ]
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***

#用户查看草稿状态的分享（1）
## 1. 业务描述：
用户查看草稿状态的分享，支持分页

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/share/draft
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
        "shares": [
            {
                *share*,
                *{sharePics}*
            },
            {
                *share*,
                *{sharePics}*
            },
            {
                *share*,
                *{sharePics}*
            },
            {
                *share*,
                *{sharePics}*
            }
        ],
        "status": "200000551",
        "info": "操作成功"
    }
}
```
***

#用户的历史分享（1）
## 1. 业务描述：
查看用户的历史分享记录，用户可以查看自己的，也可以查看他人的，支持分页

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/share/freed
请求方式：*GET*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|pageNo|Mumber|当前页码|是|
|pageSize|Mumber|每页尺寸|是|
|userId|Mumber|被查看用户ID|是|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "userId": 1000001,
        "shares": [
            {
                *share*,
                *{user(applicant)}*,
                *{takeOrder}*
            },
            {
                *share*,
                *{user(applicant)}*,
                *{takeOrder}*
            },
            {
                *share*,
                *{user(applicant)}*,
                *{takeOrder}*
            },
            {
                *share*,
                *{user(applicant)}*,
                *{takeOrder}*
            }
        ]
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***

#用户喜欢过的分享（1）
## 1. 业务描述：
查看用户like过的分享记录，分享下架与否都列出来，在返回结果里标注分享当前状态，已申请的过滤掉，用户只能查看自己的like记录，支持分页

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/share/likes
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
        "shares": [
            {
                *share*
            },
            {
                *share*
            }
        ]
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***

#用户已收到的分享（1）
## 1. 业务描述：
用户查看自己已经收到的分享记录，支持分页

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/share/received
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
        "shares": [
            {
                *share*,
                *{user}*
            },
            {
                *share*,
                *{user}*
            }
        ]
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***