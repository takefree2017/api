### 1 index
* 1 业务描述

    查询最新分享和显摆列表,按时间倒序

* 2 调用方式

    url地址：https://{domain}/takefree/v1/index
    
    请求方式：*GET*

* 3 输入参数
    
    maxShareId:最大分享id(不包含)
    
    maxShowId:最大显摆id(不包含)
    
    pageSize:可选，分页数量
    
* 4 请求消息体
    
    无

* 5 返回消息体
    ```
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": [{shareDTO/show}...]
    }
    ```
    share参见分享接口，show参见显摆接口
***
