# producer/update_runtime_options

`producer/update_runtime_options`调用可以修改出块运行参数。

注意，节点软件nodeos需要启用producer_api_plugin插件

### 调用参数
JSON对象，描述目标运行参数，其成员为：

- max_transaction_time：交易时间上限，整数
- max_irreversible_block_age：不可逆块龄上限，整数
- produce_time_offset_us：出块时间偏移量，整数，单位：微秒
- last_block_time_offset_us：最新块时间偏移量，整数，单位：微秒
- incoming_defer_ratio：滞后率，整数
- subjective_cpu_leeway_us：整数，单位：微秒

### 返回值
`get_runtime_options`调用的返回结果为描述出块运行参数的JSON对象。

### 示例代码
调用请求：
```shell
~$ curl -X POST --url http://127.0.0.1:8888/v1/producer/update_runtime_options -d '{
  "max_transaction_time": 0,
  "max_irreversible_block_age":0 ,
  "produce_time_offset_us": 0,
  "last_block_time_offset_us": 0,
  "incoming_defer_ratio": 0,
  "subjective_cpu_leeway_us": 0
}'
```

返回结果：
```json
{
    ...
}
```

