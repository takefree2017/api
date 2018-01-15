##分享种类
### 1. 业务描述：
takefree系统中大类

### 2. 调用方式：
url地址：https://{domain}/takefree/v1/sharemode?version={version}
请求方式：*GET*

### 3. 输入参数：
version 可选，最新版本，当携带此参数时，服务器端版本比version大时返回全量，否在返回码30400000。优化后不需要此参数，版本比较在客户端完成

### 4. 成功返回参数：
```
{
  "status": "20000000",
  "message": "操作成功",
  "timestamp": "2017-12-18 16:07:48",
  "result": [
    {
      "id": 1,
      "name": "实物",
      "transferable":1, //是否交接。0,否;1,是
      "participatory":1, //是否有人参与。0,否;1,是
      "small_pic_url":"", //小图标
      "pic_url":"" //大图标
    }
    ...
}
```
***
