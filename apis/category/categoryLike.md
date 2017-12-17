## 关注分类

### categorylike数据格式
```json
{
    "id": 14, //id
    "categoryId": 1, //分类id
    "userId": 1, //用户id
    "gmtCreate":"2017-11-13 11:36:02", //创建时间
    "gmtCreate":"2017-11-13 11:36:02", //最后修改时间
    "version":1 //版本
}
```
### 1 关注分类（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/categorylike

    请求方式：*POST*

* 3 输入参数
    
    categoryId //必须

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
            {categorylike}
        }
    }
    ```
***
### 2 取消关注分类（需要登录）
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/categorylike

    请求方式：*DELETE*

* 3 输入参数

    categoryId //必须
    
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
### 3 查询关注分类列表
* 1 业务描述

* 2 调用方式

    url地址：https://{domain}/takefree/v1/categorylike

    请求方式：*GET*

* 3 输入参数
    
    userId 关注人,可选
    
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
         "result": [{categorylike}...]
    }
    ```
***
