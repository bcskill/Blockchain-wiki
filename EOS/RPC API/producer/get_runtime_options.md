# producer/get_runtime_options

`producer/get_runtime_options`调用返回当前出块器的运行参数。

注意，nodeos时需要启用producer_api_plugin插件

### 调用参数
无

### 返回值
`get_runtime_options`调用的返回结果为描述出块运行参数的JSON对象。

### 示例代码
调用请求：
```shell
~$ curl -X POST --url http://127.0.0.1:8888/v1/producer/get_runtime_options
```

返回结果：
```json
{
    ...
}
```

