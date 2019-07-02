# producer/get_whitelist_blacklist

`producer/get_whitelist_blacklist`调用返回当前应用的出块白名单和黑名单。

注意，nodeos时需要启用producer_api_plugin插件。

### 调用参数
无

### 返回值
`get_whitelist_blacklist`调用返回一个JSON对象，包含出块白名单账号和黑名单账号。

### 示例代码
调用请求：
```shell
~$ curl -X POST --url http://127.0.0.1:8888/v1/producer/get_whitelist_blacklist
```

返回结果：
```json
{
    ...
}
```

