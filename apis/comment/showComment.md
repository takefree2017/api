#查看显摆的评论
## 1. 业务描述：
查看显摆的评论，暂不支持分页

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/showComment
请求方式：*GET*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|showId|Mumber|显摆ID|是|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "showId": 1000001,
        "showComments": [
            {
                *showComment*
            },
            {
                *showComment*
            }
        ]
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***