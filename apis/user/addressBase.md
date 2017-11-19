#新增（需要登录）
## 1. 业务描述：
新增地址，用户ID、省份ID、城市ID、详细地址

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/address
请求方式：*POST*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|province_id|Number|省份ID|是|
|city_id|Number|城市ID|是|
|address|String|详细地址|是|
|zip_code|String|邮编|否|
从token里取userId

# 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "addressId":1000001
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***

#更新（需要登录）
## 1. 业务描述：
修改地址信息

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/address/{{id}}
请求方式：*PUT*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|province_id|Number|省份ID|是|
|city_id|Number|城市ID|是|
|address|String|详细地址|是|
从token里取userId

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "addressId": 100000001
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***

#查看用户的所有收货地址（需要登录）
## 1. 业务描述：
查看一个用户的所有地址，暂不支持分页

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/userDTO/addresses
请求方式：*GET*

## 3. 输入参数：
无，从token里取userId

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "userId": 1000001,
        "addresses": [
            {
                *address*
            },
            {
                *address*
            }
        ]
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***

#查看地区分区字典
## 1. 业务描述：
查看地区分区字典，暂不支持分页

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/regions
请求方式：*GET*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|layer|Number|层级：10-第一层; 20-第二层|是|
|regionId|Number|区域ID|layer=20时必填；layer=10时不必填|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "userId": 1000001,
        "regions": [
            {
                *region*
            },
            {
                *region*
            }
        ]
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***
