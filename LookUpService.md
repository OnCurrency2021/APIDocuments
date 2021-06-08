# LookUpService API接口

## 注册

### 1. 查询Service

#### Request
查询服务。
查询条件包括ratings, providers 以及其他的种种。

- Method: **GET**
- URL:  ```/v1.0/lookup/?q=query```
- Headers：
- Body:
```
```

#### Response
- Body
```
{
  "services": [
    {
      "id": "",
      "type": "",
      "provider": "",
      "area": "",
      "cost": "",
      "rating": "",
      "status": "",
    },
    {},
    {}
  ]
}
```

