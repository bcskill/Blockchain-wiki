# chain/get_producers

`chain/get_producers`调用返回当前生效的出块账号信息

注意，nodeos时需要启用chain_api_plugin插件

### 调用参数
JSON对象，声明查询条件，其成员如下：

- limit：返回结果的数量上限，字符串，可选
- lower_bound：结果应当满足的下界，字符串，可选
- json：是否返回JSON对象，布尔值，默认：true

### 返回值
`get_producers`调用返回当前生效的出块账号信息

### 示例代码
调用请求：
```shell
~$ curl -X GET --url https://api.eoslaomao.com/v1/chain/get_producers
```

返回结果：
```json
{
    ...
}
```