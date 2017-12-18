### 1 获取文件名称列表
* 1 业务描述

    获取上传文件名，用于分享或显摆文件上传(不带后缀)

* 2 调用方式

    url地址：https://{domain}/takefree/v1/filename
    
    请求方式：*GET*

* 3 输入参数
    
    number 数量，默认1
    
    space 空间(share/show/comment/rate)
    
* 4 请求消息体
    
    无

* 5 返回消息体
    ```json
    {
        "status": "20000000",
        "message": "操作成功",
        "timestamp": "2017-12-18 14:44:07",
        "result": [
            "/public/takefree/share/d8a2c8f7b8454997b15b31156c5b4fb4",
            "/public/takefree/share/063522b85842487097237376bab0052b",
            "/public/takefree/share/d22b66a2f9e742fa890f03e3bf7b380d",
            "/public/takefree/share/0c7964ebb3c34fc4af540b47234b3075",
            "/public/takefree/share/ac36513a5ef749acb1ea6e087a35fa95"
        ]
    }
    ```
***
