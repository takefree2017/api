## 关注分享

### 数据格式
```json
{
    "id": 14, //id
    "shareId": 1, //分享id
    "sharePicHomepage": "/public/takefree/pic/1.jpg", 
    "shareStatus": "10",//状态。10，草稿；20，发布中；30，已送出；40，取消
    "ownerId": 2, //发布人id
    "ownerNickName": "发布人昵称",
    "ownerSmallIcon": "/public/takefree/222222.jpg", //发布人小图标
    "userId": 1, //关注人id
    "userNickName": "关注人id昵称",
    "userSmallIcon": "/public/takefree/222221.jpg", //关注人id小图标
    "gmtCreate":"2017-11-13 11:36:02" //"关注时间"
}
```
### 1 关注分享（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/sharelike

    请求方式：*POST*

* 3 输入参数
    
    shareId //必须

* 4 请求消息体
    
    无
    
* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "200000000",
        "info": "操作成功",
        "result": {
            {shareLikeDTO}
        }
    }
    ```
***
### 2 取消分享关注（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/sharelike

    请求方式：*DELETE*

* 3 输入参数

    shareId //必须
    
* 4 请求消息体
    
    无
    
* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "200000000",
        "info": "操作成功"
    }
    ```
***
### 3 查询分享关注列表
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/sharelike

    请求方式：*GET*

* 3 输入参数
    
    userId 关注人,可选
    
    shareId 可选，分享id
        
    pageSize 可选，分页数量
        
    pageNo 可选，分页号

* 4 请求消息体
    
    无
    
* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "200000000",
        "info": "操作成功",
         "result": [{shareLikeDTO}...]
    }
    ```
***
