# chain/get_currency_stats

`chain/get_currency_stats`调用返回指定代币的总体信息

注意，nodeos时需要启用chain_api_plugin插件

### 调用参数
JSON对象，声明代币合约托管账号和代币信息，成员如下：

- code：代币合约的部署账号，字符串
- symbol：要查询的代币符号，字符串

### 返回值
`get_currency_stats`调用返回指定种类代币的总体发行信息

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/chain/get_currency_stats -d '{
  "code":"eosio.token",
  "symbol": "EOS"
}'
```
参数
返回结果：
```json
{
    "EOS":{
        "supply":"1018192900.3301 EOS",
        "max_supply":"10000000000.0000 EOS",
        "issuer":"eosio"
    }
}
```