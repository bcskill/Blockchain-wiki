# net/connections

`net/connections`调用返回当前节点旳P2P连接信息。

注意，nodeos时需要启用net_api_plugin插件

### 调用参数
无

### 返回值
`connections`调用返回当前节点与其他节点旳连接信息

### 示例代码
调用请求：
```shell
~$ curl -X GET --url https://api.eoslaomao.com/v1/net/connections
```

返回结果：
```json
{
    ...
}
```

