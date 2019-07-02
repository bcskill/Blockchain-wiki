# chain/get_table_rows

`chain/get_table_rows`调用指定多索引数据表的数据行

注意，nodeos时需要启用chain_api_plugin插件

### 调用参数
JSON对象，指定数据表查询条件，其成员如下：

- scope：数据表作用域，字符串
- code：合约的托管账号名，字符串
- table：数据表名称，字符串
- table_key：键名称，字符串，可选
- json：是否返回JSON格式的结果，布尔型，默认值：true
- lower_bound：结果数据应当满足的下界值，字符串，可选
- upper_bound：结果数据应当满足的上界值，字符串，可选
- limit：返回结果数量上限，整数，默认值：10
- index_position：要使用的索引序号，例如，主键索引为1，次级索引为2，字符串，默认值：1
- key_type：索引键类型，例如uint64_t或name，字符串
- encode_type：编码类型，字符串，默认值：dec

### 返回值
`get_table_rows`调用的返回值为满足查询条件的数据行信息

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/chain/get_table_rows  -d '{
  "scope": "bcskillsurou",
  "code": "eosio",
  "table": "delband",
  "json": true
}'
```

返回结果：
```json
{
    "rows": [
        {
            "from": "bcskillsurou",
            "to": "bcskillsurou",
            "net_weight": "0.0046 EOS",
            "cpu_weight": "0.0147 EOS"
        }
    ],
    "more": false
}
```