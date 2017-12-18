# 1 基础配置信息
* 1 业务描述

    初始化信息，文件服务地址、分类版本、城市信息版本等

* 2 url

    地址：https://{domain}/takefree/v1/config
    
    请求方式：*GET*

* 3 输入参数

    无
    
* 4 请求消息体
    
    无

* 5 返回消息体
    ```json
    {
        "status": "20000000",
        "message": "操作成功",
        "timestamp": "2017-12-18 14:40:36",
        "result": [
            {
                "configItem": "category_version",
                "configValue": "1"
            },
            {
                "configItem": "picture_get_base_url",
                "configValue": "http://test-img0.qianbao.com"
            },
            {
                "configItem": "picture_update_url",
                "configValue": "https://dev-apis.qianbao.com/basicservice/v1/intranet/filer"
            },
            {
                "configItem": "region_version",
                "configValue": "1"
            }
        ]
    }
***

