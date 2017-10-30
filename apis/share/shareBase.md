***
#创建分享草稿
## 1. 业务描述：
用户创建分享，填写标题、描述，选择分享所属类目，上传分享的图片等

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/share/draft
请求方式：*POST*

## 3. 输入参数：
|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|title|String|分享的标题|否|
|ownerId|Mumber|分享者ID|是|
|description|String|分享的详细描述，数据库字段类型是text，最大长度65535个字节|否|
|categoryIds|String|类目id，分享选择多个类目时，类目ID之间用英文逗号分隔|否|
|status|String|分享当前的状态：10草稿;20发布中;30已送出|是|
|pics|IoStream|图片，一个分享可以上传多张|否|
|pics|IoStream|经度|否|
|pics|IoStream|纬度|否|
|pics|IoStream|文字地址|否|

## 4. 返回参数：
`{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "share_id": 1000001
    },
    "status": "200000551",
    "info": "操作成功"
}`
***

#更新分享草稿
## 1. 业务描述：
修改分享内容，发布分享内容

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/share/{{id}}/draft
请求方式：*PUT*

## 3. 输入参数：
*PUT* 时需要输入更新的参数

|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|title|String|分享的标题|否|
|ownerId|Mumber|分享者ID|是|
|description|String|分享的详细描述，数据库字段类型是text，最大长度65535个字节|否|
|categoryIds|String|类目id，分享选择多个类目时，类目ID之间用英文逗号分隔|否|
|status|String|分享当前的状态：10草稿;20发布中;30已送出|否|
|pics|IoStream|图片，一个分享可以上传多张|否|

## 4. 返回参数：
`{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "shareId": 1000001
    },
    "status": "200000551",
    "info": "操作成功"
}`
***

#更新分享
## 1. 业务描述：
发布分享、修改分享内容

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/share/{{id}}/
请求方式：*PUT*

## 3. 输入参数：
*PUT* 时需要输入更新的参数

|字段名|属性|描述|是否必填|
|---------|:------:|------:|------------:|
|title|String|分享的标题|是|
|ownerId|Mumber|分享者ID|是|
|description|String|分享的详细描述，数据库字段类型是text，最大长度65535个字节|是|
|categoryIds|String|类目id，分享选择多个类目时，类目ID之间用英文逗号分隔|是|
|status|String|分享当前的状态：10草稿;20发布中;30已送出|是|
|pics|IoStream|图片，一个分享可以上传多张|是|

## 4. 返回参数：
`{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "shareId": 1000001
    },
    "status": "200000551",
    "info": "操作成功"
}`
***

#查看详情
## 1. 业务描述：
查看分享信息，分享的主要信息都返回，但分享涉及的图片只返回首页url，如果想获取所有url，请使用“查看一个分享的所有图片”接口

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/share/{{id}}
请求方式：*GET*

## 3. 输入参数：
无

## 4. 返回参数：
`{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        *{share}*,
        *{sharePicUrls}*
    },
    "status": "200000551",
    "info": "操作成功"
}`
***

#查看一个分享的所有图片
## 1. 业务描述：
查看一个分享的所有图片

## 2. 调用方式：
url地址：https://dev-apis.qianbao.com/takefree/v1/share/{{id}}/pics
请求方式：*GET*

## 3. 输入参数：
无

## 4. 返回参数：
`{
    "timestamp": 1504077543058,
    "message": "操作成功",
    "result": {
        "shareId": 000001,
        *{sharePicUrls}*
    },
    "status": "200000551",
    "info": "操作成功"
}`
***