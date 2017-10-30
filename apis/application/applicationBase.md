#发送想要申请
## 1. 业务描述：
用户发送想要申请

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/application
请求方式：*POST*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|applicantId|Mumber|申请人ID|是|
|showId|Mumber|分享ID|是|
|applyType|Mumber|交易类型, 10邮寄到付; 20见面交易; 30支持两种|是|
|addressId|Mumber|申请者邮寄地址ID|否|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "applicationId": 1000001
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***

#用户的申请记录
## 1. 业务描述：
查看用户的申请记录，在返回结果里标注分享当前状态，如果分享已经下架标注是否送给了当前用户，支持分页

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/application
请求方式：*GET*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|pageNo|Mumber|当前页码|是|
|pageSize|Mumber|每页尺寸|是|
|userId|Mumber|用户ID|是|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "userId": 1000001,
        "applications": [
            {
                *application*,
                *{share}*
            },
            {
                *application*,
                *{share}*
            }
        ]
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***

#查看一个分享的申请记录
## 1. 业务描述：
查看某一个分享被申请的记录，暂不支持分页

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/application
请求方式：*GET*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|pageNo|Mumber|当前页码|是|
|pageSize|Mumber|每页尺寸|是|
|showId|Mumber|分享ID|是|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "shareId": 1000001,
        "applications": [
            {
                *application*
            },
            {
                *application*
            }
        ]
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***