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

以account_action_seq为查询的primary_key，

返回从pos指定的id开始，到pos+offset区间内的记录。

如果pos为-1，及为倒序查询，offset也是为负数，及向前倒着查询。

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://nodes.get-scatter.com/v1/history/get_actions -d '{
  "pos": 1,
  "offset": 1,
  "account_name": "bcskillsurou",
  "json": true
}'
```

返回结果：
```json
{
    "actions": [
        {
            "global_action_seq": 1097094232,
            "account_action_seq": 1,
            "block_num": 24829814,
            "block_time": "2018-11-02T12:16:43.500",
            "action_trace": {
                ....
            }
        },
        {
            "global_action_seq": 1127555831,
            "account_action_seq": 2,
            "block_num": 24993101,
            "block_time": "2018-11-03T10:59:22.000",
            "action_trace": {
                ....
            }
        }
    ],
    "last_irreversible_block": 66669805
}
```