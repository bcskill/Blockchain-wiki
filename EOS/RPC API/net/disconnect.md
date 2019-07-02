# net/disconnect

`net/disconnect`调用可以断开与指定eos节点的连接。

注意，nodeos时需要启用net_api_plugin插件

### 调用参数
`disconnect`的参数为要断开连接的节点地址

### 返回值
...

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://127.0.0.1:8888/v1/net/disconnect -d 1.2.3.4:9876
```

返回结果：
```json
{
    ...
}
```

