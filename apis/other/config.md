# 1 基础配置信息
* 1 业务描述

    初始化信息，文件服务地址、分类版本、城市信息版本等

* 2 调用方式

    url地址：https://{domain}/takefree/v1/filename
    
    请求方式：*GET*

* 3 输入参数
    
    number:文件数,默认1
    
    space:空间(share/rate/show/common)
    
* 4 请求消息体
    
    无

* 5 返回消息体
    ```json
    {
        "timestamp": "2017-11-13 11:36:02",
        "message": "操作成功",
        "status": "20000000",
        "info": "操作成功",
        "result": ["filename1","filename2"]
    }
    ```
***
