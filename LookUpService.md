# LookUpService API接口

### 1. 查询Service

#### Request
查询服务。
查询条件包括ratings, providers 以及其他的种种。

- Method: **GET**
- URL:  ```/v1.0/lookup/service```
- Headers：
- Body:
```
```

#### Response
- Body
```
{
  "code": 200,
  "data": {
    "services": [
      {
        "id": "",
        "type": "",
        "provider": "",
        "area": "",
        "cost": "",
        "rating": "",
        "status": "",
      },{},{}]
  "message": "providers returned"
}
```


### 2. 查询Consumer

#### Request


- Method: **GET**
- URL:  ```/v1.0/lookup/consumer```
- Headers：
- Body:
```
```

#### Response
- Body
```
{
  "code": 200,
  "data": {
    "consumers": [{
      "id": "",
      "name": "",
      "address": "",
      "mobile": "",
      "email": ""
    },{},{}]
  "message": "providers returned"
}
```

### 3. 查询Provider

#### Request


- Method: **GET**
- URL:  ```/v1.0/lookup/provider```
- Headers：
- Body:
```
```

#### Response
- Body

```
{
  "code": 200,
  "data": {
    "providers": [{
        "id": "",
        "name": "",
        "mobile": "",
        "activesince": "2021-06-08"
      },{}]
  },
  "message": "providers returned"
}
```

### 4. 查询Order

#### Request


- Method: **GET**
- URL:  ```/v1.0/lookup/order```
- Headers：
- Body:
```
```
#### Response
- Body
```
{
  "code": 200,
  "data": {
    "orderId": "123",
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
  "message": "services returned"
}

```


## 消息队列数据

### 1. Consumer Service

#### data

JSON格式数据.

```
{
  "action":"CREATE",
  "data": {
      "id": "",
      "name": "",
      "address": "",
      "mobile": "",
      "email": ""
   }
}
```


### 2. Provider Service

#### data

JSON格式数据.

```
{
  "action":"CREATE",
  "data": {
      "id": "",
      "name": "",
      "address": "",
      "mobile": "",
      "email": ""
    }
}
```

### 3. Service Service

#### data

```
{
  "action":"CREATE",
  "data": {
      "id": "",
      "type": "",
      "provider": "",
      "area": "",
      "cost": "",
      "rating": "",
      "status": "",
  }
}
```

### 4. Order Service

#### create data

```
{
  "action":"CREATE",
  "data": {
    "orderId": "123"
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
}
```

#### update data

```
{
  "action":"UPDATE",
  "data": {
    "orderId": "123",
    "status" : "finished"
  }
}
```

