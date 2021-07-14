# API接口

## Service Service

### 1.创建特定服务

创建一个特定服务

#### Request
- Method: **POST**
- URL:  ```/v1.0/service```
- Headers：Content-Type:application/json;charset=utf-8
- Body:
```
{
    "type" : "家政服务3",
    "provider":"f21eca-uwqeqcqa1-c2312cas-k2e12cq",
    "area": "上海市杨浦区",
    "cost" : "50",
    "status" : "active",
    "rating": "1"
}
```

#### Response
- Body
```
{
  "code": 200,
  "data": {
     "id":"123"
  },
  "message": "new service has created"
}
```

### 2.获取特定服务

**获取特定服务的方式**

目前有1种获取特定服务的方式：
- 根据特定服务的ID获取特定服务： service

#### Request

- Method: **GET**
- URL: ```/v1.0/service/{id}```
- Headers:
- Body:
```
```

#### Response
- Body
```
{
    "id": "f21eca-uwqeqcqa1-c2312cas-k2e12cq"
    "type" : "家政服务3",
    "provider":"123",
    "area": "上海市杨浦区",
    "cost" : "50",
    "status" : "active",
    "rating": "1"
}
```

