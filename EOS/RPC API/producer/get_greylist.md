# producer/get_greylist

`producer/get_greylist`调用返回出块灰名单。

注意，nodeos时需要启用producer_api_plugin插件

### 调用参数
无

### 返回值
`get_greylist`调用返回当前启用的出块灰名单。

### 示例代码
调用请求：
```shell
~$ curl -X POST --url http://127.0.0.1:8888/v1/producer/get_greylist
```

返回结果：
```json
{
    "accounts":["a11111111111","aaa","bbb"]
}
```

