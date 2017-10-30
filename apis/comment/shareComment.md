#查看分享的评论
## 1. 业务描述：
查看分享的评论，暂不支持分页

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/shareComment
请求方式：*GET*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|shareId|Mumber|分享ID|是|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "shareComments": [
            {
                *shareComment*
            },
            {
                *shareComment*
            }
        ]
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***