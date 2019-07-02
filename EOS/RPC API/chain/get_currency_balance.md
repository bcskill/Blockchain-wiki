# chain/get_currency_balance

`chain/get_currency_balance`调用返回指定账户的代币余额信息

注意，nodeos时需要启用chain_api_plugin插件

### 调用参数
JSON对象，用来声明查询参数，其成员如下：

- code：代币合约托管账户名称，字符串
- account：要查询账户的名称，字符串
- symbol：要查询的代码符号，字符串

### 返回值
`get_currency_balance`调用返回指定账号所持有的代币余额

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/chain/get_currency_balance -d '{
  "code":"eosio.token",
  "account": "eosio",
  "symbol": "EOS"
}'
```

返回结果：
```json
["1813.6530 EOS"]
```

