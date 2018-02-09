### 权限
* 接口权限通过token验证，tokenId在登录时返回，同时设置cookie。
* 对于权限验证的接口通过cookie或者http参数方式携带takefree_token。token过期或无效返回401000000错误
* 为了控制数据权限,userId字段通过token获取

> 接口访问权限在每个接口单独标注，未标注代表不需要登录

### 请求格式
需要调用方提供身份信息
> HTTP Header 
> Uni-Source: 产品名称/运行环境 (附加信息)
* 产品名称:takefree
* 运行环境可选值：Android、iOS、H5、Server(当代码运行在服务器上时)
* 附加信息:app版本，系统版本等

请求body格式为json
> Content-type: application/json;charset=utf-8

### 响应格式
响应body格式为json，参见[resthub](http://wiki.qianbaoqm.com/pages/viewpage.action?pageId=14190569)
* 格式1（map）
    ```json
    {
     "status":"20000000",
     "timestamp": "2017-11-13 11:36:02",
     "message":"OK",
     "result":{"col_1":"val_1", "col_2":"val_2"},
     "info":"xxx"
     }
    ```
* 格式2（list[map]）
    ```json
    {
     "status":"20000000",
     "timestamp": "2017-11-13 11:36:02",
     "message":"OK",
     "result":[{"col_1":"val_1","col_2":"val_2"},{"col_1":"val_1","col_2":"val_2"}],
     "info":"xxx"
     }
    ```
***
> result内容在各接口定义

> status规范
* 第一位是HTTP语义(2x,成功;3xx,资源重定向;4xx,请求错误;5xx,服务器内部错误)
* 第二、第三位，一级错误分类。暂未使用，00
* 第四、五位，二级错误分类。暂未使用，00
* 第六、七位，八位，业务分类，本应用统一为000

