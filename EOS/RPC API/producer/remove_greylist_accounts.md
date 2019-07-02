# producer/remove_greylist_accounts

`producer/remove_greylist_accounts`调用从出块灰名单中删除指定的账号。

注意，节点软件nodeos需要启用producer_api_plugin插件。

### 调用参数
JSON对象，声明要添加到灰名单中的账号，其成员为：

- accounts：字符串数组，每个成员指定一个账号

### 返回值
...

### 示例代码
调用请求：
```shell
~$ curl -X POST --url http://127.0.0.1:8888/v1/producer/remove_greylist_accounts -d '{
  "accounts": ["aaa","bbb"]
}'
```

返回结果：
```json
{
    ...
}
```

