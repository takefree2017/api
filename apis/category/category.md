##类目
### 1. 业务描述：
takefree系统中分享物品的类目

### 2. 调用方式：
url地址：https://{domain}/takefree/v1/category?version={version}
请求方式：*GET*

### 3. 输入参数：
version为可选参数,表示请求端的已有数据版本。

### 4. 成功返回参数：
```
{
  "status": "20000000",
  "message": "操作成功",
  "timestamp": "2017-12-18 16:07:48",
  "result": [
    {
      "id": 100000,
      "categoryName": "电脑数码",
      "layer": 10,
      "parentCategoryId": 0,
      "virtualFlag":	1,
      "express":	1,
      "participant":	1,
      "subCategoryList": [
        {
          "id": 101000,
          "categoryName": "手机通讯",
          "layer": 20,
          "parentCategoryId": 0,
          "virtualFlag":	1,
          "express":	0,
          "participant":	0
        },
        {
          "id": 101100,
          "categoryName": "摄影摄像",
          "layer": 20,
          "parentCategoryId": 0,
          "virtualFlag":	0,
          "express":	0,
          "participant":	0
        },
        ...
    }
    ...
}
```
***
