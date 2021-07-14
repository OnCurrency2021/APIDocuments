# API接口

## Consumer Service

### 1.创建服务消费者

创建一个服务消费者

#### Request
- Method: **POST**
- URL:  ```/v1.0/consumer```
- Headers：Content-Type:application/json
- Body:
```
{
    "name" : "消费者",
    "address" : "上海市杨浦区邯郸路220号",
    "mobile" : "12345678901",
    "email" : "12345678901@fudan.edu.cn",
    "area":"杨浦区"
}
```

#### Response
- Body
    - 成功创建服务消费者
    ```
    {
      "code": 200,
      "data": {
         "id":"123"
      },
      "message": "Creating new service consumer success!"
    }
    ```

    - 创建服务消费者失败
    ```
    {
      "code": 1000,
      "message": "Creating new service consumer failed!"
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

    - 存在对应id的服务消费者
    ```
    {
      "code": 200,
      "data": {
        "name" : "消费者",
        "address" : "上海市杨浦区邯郸路220号",
        "mobile" : "12345678901",
        "email" : "12345678901@fudan.edu.cn",
        "area":"杨浦区"
      },
      "message": "OK!"
    }
    ```
  
    - 不存在对应id的服务消费者
    ```
    {
      "code": 1001,
      "message": "No service consumer found!"
    }
    ```
