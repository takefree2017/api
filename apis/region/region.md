##地区编码
## 1. 业务描述：
全国所有省市编码

### 2. 调用方式：
url地址：https://{domain}/takefree/v1/region?version={version}
请求方式：*GET*

### 3. 输入参数：
version为可选参数，表示请求端已有数据的版本。

### 4. 成功返回参数：
```
{
  "status": "20000000",
  "message": "操作成功",
  "timestamp": "2017-12-18 15:41:47",
  "result": [
    {
      "id": 110000,
      "regionName": "北京市",
      "layer": 10,
      "parentRegionId": 0,
      "subRegionList": [
        {
          "id": 110101,
          "regionName": "东城区",
          "layer": 30,
          "parentRegionId": 110000
        },
        {
          "id": 110102,
          "regionName": "西城区",
          "layer": 30,
          "parentRegionId": 110000
        },
        ...
    }
    ...
}
```
***

