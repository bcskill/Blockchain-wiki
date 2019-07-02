# history/get_actions

`history/get_actions`调用返回指定合约上执行过的动作

注意，nodeos时需要启用history_api_plugin插件，并且设置filter-on选项

### 调用参数
JSON对象，指定查询参数，其成员如下：

- pos：位置，整数
- offset：偏移量，整数
- account_name：合约托管账号，字符串

### 返回值
`get_actions`调用的返回值为指定账号的托管合约上发生过的历史动作调用。

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/history/get_actions -d '{
  "pos": -1,
  "offset": -20,
  "account_name": "eosio"
}'
```

返回结果：
```json
{
  ...
}
```