# chain/get_table_by_scope

`chain/get_table_by_scope`调用返回多索引数据表中满足指定查询条件的数据行

### 调用参数
JSON对象，指定数据表查询条件，其成员如下：

- code：合约的托管账号名，字符串
- table：数据表名称，字符串
- lower_bound：结果数据应当满足的下界值，字符串，可选
- upper_bound：结果数据应当满足的上界值，字符串，可选
- limit：返回结果数量上限，整数，默认值：10

### 返回值
`get_table_by_scope`调用的返回值为满足查询条件的数据行信息

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/chain/get_table_by_scope -d '{
  "code": "eosio.token",
  "table": "accounts"
}'
```

返回结果：
```json
{
    "rows":[
        {
            "code":"eosio.token",
            "scope":"..........e",
            "table":"accounts",
            "payer":"lovestarteos",
            "count":1
        },
        {
            "code":"eosio.token",
            "scope":"..........m",
            "table":"accounts",
            "payer":"m",
            "count":1
        },
        {
            "code":"eosio.token",
            "scope":"..........tp",
            "table":"accounts",
            "payer":"itokenpocket",
            "count":1
        },
        {
            "code":"eosio.token",
            "scope":".........a.e",
            "table":"accounts",
            "payer":"buyname.io",
            "count":1
        },
        {
            "code":"eosio.token",
            "scope":".........e.e",
            "table":"accounts",
            "payer":"e",
            "count":1
        },
        {
            "code":"eosio.token",
            "scope":".......e.e",
            "table":"accounts",
            "payer":"ieooooooooos",
            "count":1
        },
        {
            "code":"eosio.token",
            "scope":".......q",
            "table":"accounts",
            "payer":"q",
            "count":1
        },
        {
            "code":"eosio.token",
            "scope":"......q",
            "table":"accounts",
            "payer":"q",
            "count":1
        },
        {
            "code":"eosio.token",
            "scope":".....q",
            "table":"accounts",
            "payer":"q",
            "count":1
        },
        {
            "code":"eosio.token",
            "scope":".....tp",
            "table":"accounts",
            "payer":"xiaodan11111",
            "count":1
        }
    ],
    "more":"....q"
}
```