#首页list接口
## 1. 业务描述：
首页上按时间排序所有正在进行的分享和显摆，支持分页

## 2. 调用方式：
url地址：https://{domain}/takefree/v1/pageview
请求方式：*GET*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|shareId|Mumber|分享当前的ID|是|
|showId|Mumber|显摆当前的ID|是|
|pageSize|Mumber|每页尺寸|是|
|viewType|Mumber|用于表示内容种类：10-只看显摆，20-只看分享，30-显摆和分享都看|是|

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
        ],
        "shows":[
            {
                *show*
            },
            {
                *show*
            }
        ]
    },
    "status": "20000000",
    "info": "操作成功"
}
```
***
