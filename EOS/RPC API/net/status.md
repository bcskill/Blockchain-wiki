# net/status

`net/status`调用返回当前节点旳P2P网络状态。

注意，节点软件nodeos需要启用met_api_plugin插件

### 调用参数
无

### 返回值
`status`调用的返回值为一个描述网络状态的JSON对象

### 示例代码
调用请求：
```shell
~$ curl -X POST --url http://127.0.0.1:8888/v1/net/status
```

返回结果：
```json
{
    ...
}
```

