## 分享订单

### order数据格式
```json
{
    "id": 14, //id
    "shareId": 1, //分享id
    "sharePicHomepage": "", //分享首页图片
    "ownerId": 1, //分享者id
    "ownerNickName": "分享者昵称", 
    "ownerSmallIcon": "分享者小图标", 
    "applicantId": 2, //申请人id
    "applicantNickName": "申请人昵称", 
    "applicantSmallIcon": "申请人小图标", 
    "takeTime": "2017-11-13 11:36:02", //订单时间
    "applyType": 10, //10邮寄到付; 20见面交易; 30支持两种
    "addressId": 1, //收货地址
    "status": 10, //10,初始状态;20,成功;30,申请失败
    "logisticsStatus": 20, //10,无物流单；20，有物流单
    "rateStatus": 10, //10未评价，20已评价
    "rate":1,//评价，1好评 0差评
    "showStatus": 1, //10,未显摆 20,已显摆
    "gmtCreate":"2017-11-13 11:36:02", //创建时间
    "gmtCreate":"2017-11-13 11:36:02", //最后修改时间
    "version":1 //版本
}
```

### 1 创建订单（需要登录，发布人调用）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/order

    请求方式：*POST*

* 3 输入参数
    
    无

* 4 请求消息体
    ```json
    {
        "shareId": 1, //分享id
        "users": [10,20,30] //申请人id
    }
    ```

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
### 2 删除订单（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/order/{id}

    请求方式：*DELETE*

* 3 输入参数
    
    无

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
### 3 修改订单（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/order/{id}

    请求方式：*PUT*

* 3 输入参数
    
    无

* 4 请求消息体
    
    {
        "status": 20
    }

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
### 4 根据id查询订单（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/order/{id}

    请求方式：*GET*

* 3 输入参数
    
    无

* 4 请求消息体
    
    {
        "applyType": 10,
        "status": 20
            
    }

* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "200000000",
        "info": "操作成功",
        "result": {
             "{order}"
        }
    }
    ```
***
### 5 查询订单列表（需要登录）
* 1 业务描述

    查询用户收到的分享列表，可根据发布人筛选

* 2 调用方式

    url地址：https://{domain}/takefree/v1/order

    请求方式：*GET*

* 3 输入参数
    
    applicantId:可选,申请人id
    
    shareId:可选,分享id
    
    status:可选,状态
    
    pageSize:可选，分页数量
    
    pageNo:可选，分页号
    
* 4 请求消息体
    
    无

* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": [{order}...]
    }
    ```
***
