#创建订单
## 1. 业务描述：
分享者从申请人列表里选择一个用户，做分享送出操作

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/takeorder
请求方式：*POST*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|shareId|Mumber|分享ID|是|
|applicantId|Mumber|申请人ID|是|
|applicationId|Mumber|申请单ID|是|
|addressId|Mumber|送货地址ID|否|
|takeType|Mumber|交易类型：10邮寄到付; 20见面交易|否|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "takeOrderId": 1000001
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***

#更新订单
## 1. 业务描述：
更新订单状态，例如已评价、已显摆等

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/takeorder/{{id}}
请求方式：*PUT*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|status|Number|20发布者已填运单号; 30申请人已评价; 40申请人已显摆; 40已评价并已显摆|否|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "takeOrderId": 1000001
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***