#用户关注类目（需要登录）
## 1. 业务描述：
用户设置个人喜好，新增关注类目

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/category/{{id}}/like
请求方式：*POST*

## 3. 输入参数：
无，从token里取userId

## 4. 成功返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "categoryLikeId": 1000001
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***

#用户关注类目（需要登录）
## 1. 业务描述：
用户设置个人喜好，新增关注类目

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/category/{{id}}/like
请求方式：*DELETE*

## 3. 输入参数：
无，从token里取userId

## 4. 成功返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "categoryLikeId": 1000001
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***
