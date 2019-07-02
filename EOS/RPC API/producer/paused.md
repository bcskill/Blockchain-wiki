# producer/paused

`producer/paused`调用返回当前出块器是否暂停。

注意，nodeos时需要启用producer_api_plugin插件

### 调用参数
无

### 返回值
...

### 示例代码
调用请求：
```shell
~$ curl -X POST --url http://127.0.0.1:8888/v1/producer/paused
```

返回结果：
```json
{
    ...
}
```

