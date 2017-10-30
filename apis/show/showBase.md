#创建
## 1. 业务描述：
用户对已经收到的分享显摆一下，上传物品图片、描述、选择一个心情图标

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/show
请求方式：*POST*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|orderId|Mumber|分享ID|是|
|receiverId|Mumber|被赠者ID|是|
|giverId|Mumber|赠送者ID|是|
|moodId|Mumber|心情图标ID|是|
|content|String|分享的详细描述，数据库字段类型是text，最大长度65535个字节|否|
|pics|IoStream|图片，一个分享可以上传多张|是|

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "show_id": 1000001
    },
    "status": "200000551",
    "info": "操作成功"
}
```
***

#查看
## 1. 业务描述：
查看显摆信息，但不包括显摆的评论

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/show/{{id}}
请求方式：*GET*

## 3. 输入参数：
无

## 4. 返回参数：
```
{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        *show*
    }
    "status": "200000551",
    "info": "操作成功"
}
```
***