# chain/get_required_keys

`chain/get_required_keys`调用返回签名一个交易时需要的公钥清单

注意，nodeos时需要启用chain_api_plugin插件

### 调用参数
JSON对象，用来声明要签名的交易和可用的公钥集合，其成员如下：

- transaction：交易数据，JSON对象
- available_keys：可用公钥，数组

### 返回值
`get_required_keys`返回一组必须的用于签名的公钥

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/chain/get_required_keys -d '{
  "transaction": {
    "ref_block_num": "100",
    "ref_block_prefix": "137469861",
    "expiration": "2017-09-25T06:28:49",
    "scope": ["initb", "initc"],
    "actions": [{
      "code": "currency",
      "type": "transfer",
      "recipients": ["initb", "initc"],
      "authorization": [{
        "account": "initb",
        "permission": "active"
      }],
      "data": "000000000041934b000000008041934be803000000000000"
    }],
    "signatures": [],
    "authorizations": []
  },
  "available_keys": [
    "EOS4toFS3YXEQCkuuw1aqDLrtHim86Gz9u3hBdcBw5KNPZcursVHq",
    "EOS7d9A3uLe6As66jzN8j44TXJUqJSK3bFjjEEqR4oTvNAB3iM9SA",
    "EOS6MRyAjQq8ud7hVNYcfnVPJqcVpscN5So8BhtHuGYqET5GDW5CV"]
}'
```

返回结果：
```json
{
  "required_keys": [
    "EOS6MRyAjQq8ud7hVNYcfnVPJqcVpscN5So8BhtHuGYqET5GDW5CV"
  ]
}
```