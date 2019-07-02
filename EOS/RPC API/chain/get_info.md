## chain/get_info
chain/get_info调用返回区块链总体信息。
### 调用参数
无
### 返回值
get_info调用的返回结果是一个JSON对象，包含当前所连接EOS链的总体信息，成员如下：

- server_version：节点版本
- head_block_num：链头区块序号
- lase_irreversible_block_num：最后不可逆区块号
- head_block_id：链头区块ID
- head_block_time：链头区块生成时间
- head_block_producer：链头区块出块账号

### 示例代码
调用请求：
```shell
~$ curl -X GET --url https://api.eoslaomao.com/v1/chain/get_info
```

返回结果：
```json
{
    "server_version":"5d06142c",
    "chain_id":"aca376f206b8fc25a6ed44dbdc66547c36c6c33e3a119ffbeaef943642f0e906",
    "head_block_num":66496465,
    "last_irreversible_block_num":66496129,
    "last_irreversible_block_id":"03f6a6812c29cc6f98825e79d436134b972857c8512cb28473af6c1109db03fd",
    "head_block_id":"03f6a7d18b4b758ef30a97b50dc0e43e324792a60a4087ff6102487954767b25",
    "head_block_time":"2019-07-02T03:28:17.500",
    "head_block_producer":"eoscannonchn",
    "virtual_block_cpu_limit":160604763,
    "virtual_block_net_limit":1048576000,
    "block_cpu_limit":200000,
    "block_net_limit":1048576,
    "server_version_string":"v1.6.1-575-g5d06142c5"
}
```