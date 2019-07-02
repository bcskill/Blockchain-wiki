# chain/abi_bin_to_json

`chain/abi_bin_to_json`调用将16进制码流反序列化为合约的动作调用

注意，nodeos时需要启用chain_api_plugin插件

### 调用参数
JSON对象，用来声明要进行序列化的合约动作调用，其成员如下：

- code：合约托管账号名称，字符串
- action：要调用的合约动作名称，字符串
- args：合约动作参数，16进制码流，字符串

### 返回值
`abi_bin_to_json`调用的返回结果为反序列化后的合约动作调用对象

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/chain/abi_bin_to_json -d '{
  "code":"eosio.token",
  "action":"transfer",
  "args": "0000000000ea30550000000000ea3055809698000000000004454f5300000000027878"
}'
```

返回结果：
```json
{
  "from": "eosio",
  "to": "eosio",
  "quantity": "1000.0000 EOS",
  "memo": "xx"
}
```