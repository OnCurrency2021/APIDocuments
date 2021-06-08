# API接口

## Order Service

### 1.创建订单服务

创建一个订单服务

#### Request
- Method: **POST**
- URL:  ```/v1.0/order
- Headers：Content-Type:application/json
- Body:
```
{
    "serviceId":"123",
    "providerId":"123",
    "consumerId":"123",
    "timeSlot":{
       "start":"8:00",
       "end":"12:00"
    },
    "cost":"200",
    "status" : "active"
}
```

订单状态：active 和 finished

#### Response
- Body
```
{
  "code": 200,
  "data": {
     "id":"123"
  },
  "message": "new order has created"
}
```

### 2.获取订单

**获取订单的方式**

目前有1种获取订单的方式：
- 根据订单的ID获取订单： order

#### Request

- Method: **GET**
- URL: ```/v1.0/order?id={id}```
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
    "serviceId":"123",
    "providerId":"123",
    "consumerId":"123",
    "timeSlot":{
       "start":"8:00",
       "end":"12:00"
    },
    "cost":"200",
    "status" : "active"
  },
  "message": "OK"
}
```

### 3.完成订单

完成一个订单

#### Request
- Method: **PUT**
- URL:  ```/v1.0/order
- Headers：Content-Type:application/json
- Body:
```
{
    "id":"123"
}
```

#### Response
- Body
```
{
  "code": 200,
  "message": "order 123 has been finished"
}
```

