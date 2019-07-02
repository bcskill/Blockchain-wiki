# chain/push_block

`chain/push_block`调用将指定的区块数据提交到链上

注意，节点软件nodeos需要启用chain_api_plugin插件

### 调用参数
JSON对象，声明要提交的区块数据，成员如下：

- timestamp：区块时间戳，时间字符串
- producer：出块账号，字符串
- confirmed
- previous
- transaction_mroot
- action_mroot
- block_mroot
- version
- new_producers：新出现的出块账号集合，空或数组
- header_extensions
- producer_signature：出块账号的签名，字符串
- transactions：区块中包含的交易集合，数组
- block_extensions

### 返回值


### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/chain/push_block -d '{
  ...
}'
```

返回结果：
```json
{
    ...
}
```