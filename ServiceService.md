# API接口

## Service Service

### 1.创建特定服务

创建一个特定服务

#### Request
- Method: **POST**
- URL:  ```/v1.0/service
- Headers：Content-Type:application/json
- Body:
```
{
    "type" : "家政服务",
    "providerId":"123"
    "serviceArea" : [
           "杨浦区"，
           "宝山区"
    ],
    "hourlyCost" : 50,
    "status" : "active",
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
- URL: ```/v1.0/service?id={id}```
- Headers:
- Body:
```
```

#### Response
- Body
```
{
  "code": 200,
  "data": {
    "type" : "家政服务",
    "providerId":"123"
    "serviceArea" : [
           "杨浦区"，
           "宝山区"
    ],
    "hourlyCost" : 50,
    "status" : "active",
    "overallRating":4.6
  },
  "message": "OK"
}
```

