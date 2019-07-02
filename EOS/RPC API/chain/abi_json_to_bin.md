# chain/abi_json_to_bin

`chain/abi_json_to_bin`调用将合约动作调用序列化为16进制字符串，以便应用于 `push_action`调用

注意，nodeos时需要启用chain_api_plugin插件

### 调用参数
JSON对象，用来声明要进行序列化的合约动作调用，其成员如下：

- code：合约托管账号名称，字符串
- action：要调用的合约动作名称，字符串
- args：合约动作参数，JSON对象

### 返回值
`abi_json_to_bin`调用的返回结果为序列化字符串

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/chain/abi_json_to_bin -d '{
  "code": "eosio.token",
  "action":"transfer",
  "args": {"from":"eosio","to":"eosio","quantity":"1000.0000 EOS","memo":"xx"}
}'
```

返回结果：
```json
{
    "binargs":"0000000000ea30550000000000ea3055809698000000000004454f5300000000027878"
}
```