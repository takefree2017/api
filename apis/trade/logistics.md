#填写物流单
## 1. 业务描述：
分享者从申请人列表里选择一个用户，做分享送出操作

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/logistics
请求方式：*POST*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|orderId|Number|订单ID|是|
|logisticsNumber|String|物流单号|是|
|status|Number|物流状态, 10送货中; 20妥投|否|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "logisticsId": 1000001
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***

#更新物流单
## 1. 业务描述：
物流状态更新

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/logistics
请求方式：*PUT*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|status|Number|物流状态, 10送货中; 20妥投|否|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "logisticsId": 1000001
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***