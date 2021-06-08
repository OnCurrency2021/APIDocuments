# API接口

## Consumer Service

### 1.创建服务消费者

创建一个服务消费者

#### Request
- Method: **POST**
- URL:  ```/v1.0/consumer
- Headers：Content-Type:application/json
- Body:
```
{
    "name" : "消费者",
    "address" : "上海市杨浦区邯郸路220号",
    "mobile" : "12345678901",
    "email" : "12345678901@fudan.edu.cn",
    "geoLocation" : {
       "longitude":121.48 ,
       "latitude":31.23
    },
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
  "message": "new consumer has created"
}
```

### 2.获取消费者

**获取服务消费者的方式**

目前有1种获取服务消费者的方式：
- 根据服务消费者的ID获取服务消费者： consumer

#### Request

- Method: **GET**
- URL: ```/v1.0/consumer?id={id}```
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
    "name" : "消费者",
    "address" : "上海市杨浦区邯郸路220号",
    "mobile" : "12345678901",
    "email" : "12345678901@fudan.edu.cn",
    "geoLocation" : {
       "longitude":121.48 ,
       "latitude":31.23
    },
  },
  "message": "OK"
}
```

