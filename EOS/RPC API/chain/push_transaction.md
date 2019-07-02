# chain/push_transaction

`chain/push_transaction`调用将指定的交易提交到链上

注意，节点软件nodeos需要启用chain_api_plugin插件

### 调用参数
JSON对象，声明交易、签名等信息，成员如下：

- signatures：签名数组
- compression：是否压缩格式，布尔类型，默认值：false
- packed_context_free_data：上下文无关的数据
- packed_tx：序列化的交易数据

### 返回值
`push_transaction`调用的返回结果包含交易ID

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/chain/push_transaction -d '{
  ...
}'
```

返回结果：
```json
{
    'transaction_id' = "1..."
}
```