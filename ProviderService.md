# API接口

## Provider Service

### 1.创建服务提供者

创建一个服务提供者

#### Request
- Method: **POST**
- URL:  ```/v1.0/provider```
- Headers：Content-Type:application/json
- Body:
```
{
    "name" : "提供者",
    "mobile" : "12345678901",
    "activeSince":"2021-06-08",
}
```
 
#### Response
- Body

    - 成功创建服务提供者
    ```
    {
      "code": 200,
      "data": {
         "id":"123"
      },
      "message": "Creating new service provider success!"
    }
    ```
  
    - 创建服务提供者失败
    ```
    {
      "code": 1000,
      "message": "Creating new service provider failed!"
    }
    ```

### 2.获取消费者

**获取服务提供者的方式**

目前有1种获取服务提供者的方式：
- 根据服务提供者的ID获取服务提供者： provider

#### Request

- Method: **GET**
- URL: ```/v1.0/provider?id={id}```
- Headers:
- Body:
```
```

#### Response
- Body

    - 存在对应id的服务提供者
    ```
    {
      "code": 200,
      "data": {
        "name" : "提供者",
        "mobile" : "12345678901",
        "activeSince":"2021-06-08",
      },
      "message": "OK!"
    }
    ```
  
    - 不存在对应id的服务提供者
    ```
    {
      "code": 1001,
      "message": "No service provider found!"
    }
    ```
