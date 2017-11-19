#填写物流单（需要登录）
## 1. 业务描述：
赠与人交易达成后，给订单补增物流单号

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/logistics
请求方式：*POST*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|orderId|Number|订单ID|是|
|logisticsNumber|String|物流单号|是|
|status|Number|物流状态, 10送货中; 20妥投|否|
从token里取userId，判断当前用户是否是赠与人

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "logisticsId": 1000001
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***

#更新物流单（需要登录）
## 1. 业务描述：
物流状态更新

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/logistics
请求方式：*PUT*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|status|Number|物流状态, 10送货中; 20妥投|否|
从token里取userId，受赠人和后台物流匹配任务可以操作

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "logisticsId": 1000001
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***
