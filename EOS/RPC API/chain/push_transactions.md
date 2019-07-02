# chain/push_transactions

`chain/push_transactions`调用将一组交易提交到链上

注意，节点软件nodeos需要启用chain_api_plugin插件

### 调用参数
JSON对象，指定一组要提交的交易，成员如下：

- body

### 返回值
`push_transactions`调用的返回值包含交易ID

### 示例代码
调用请求：
```shell
~$ curl -X POST --url http://127.0.0.1:8888/v1/chain/push_transactions -d '{
  ...
}'
```

返回结果：
```json
{
    'transaction_id' = "1..."
}
```