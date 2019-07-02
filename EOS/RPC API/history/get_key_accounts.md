# history/get_actions

`history/get_key_accounts`调用返回指定公钥所关联的账号。

注意，nodeos时需要启用history_api_plugin插件，并且设置filter-on选项

### 调用参数
JSON对象，声明要查询的公钥，其成员为：

- public_key：公钥，字符串

### 返回值
`get_key_accounts`调用的返回值为一组关联指定公钥的账号

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/history/get_key_accounts -d '{
  "public_key": "..."
}'
```

返回结果：
```json
{
  ...
}
```