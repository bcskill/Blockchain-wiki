# history/get_transaction

`history/get_transaction`调用返回指定的交易数据。

注意，nodeos时需要启用history_api_plugin插件，并且设置filter-on选项

### 调用参数
JSON对象，声明要查询的交易，其成员如下：

- id：交易ID，字符串

### 返回值
`get_transaction`调用的返回值为查询到的交易描述JSON对象

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/history/get_transaction  -d '{
  "id": "...."
}'
```

返回结果：
```json
{
  ...
}
```