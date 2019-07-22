# history/get_transaction

`history/get_transaction`调用返回指定的交易数据。

注意，nodeos时需要启用history_api_plugin插件，并且设置filter-on选项

### 调用参数
JSON对象，声明要查询的交易，其成员如下：

- id：交易ID，字符串
- block_num_hint：交易所在块id

### 返回值
`get_transaction`调用的返回值为查询到的交易描述JSON对象

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/history/get_transaction  -d '{
 "id": "43edee11cd8b85c5a963d58c0d7d437067f0018294ef1dd13533980b2763c0f0",
 "block_num_hint":69986424
}'
```

返回结果：
```json
{
    "id": "43edee11cd8b85c5a963d58c0d7d437067f0018294ef1dd13533980b2763c0f0",
    "trx": {
        "receipt": {
            "status": "executed",
            "cpu_usage_us": 189,
            "net_usage_words": 6,
            "trx": [
                0,
                "43edee11cd8b85c5a963d58c0d7d437067f0018294ef1dd13533980b2763c0f0"
            ]
        }
    },
    "block_time": "2019-07-22T09:01:47.500",
    "block_num": 69986424,
    "last_irreversible_block": 69986246,
    "traces": []
}
```