# net/connect

`net/connect`调用的作用是让当前节点连接指定的eos节点。

注意，nodeos时需要启用net_api_plugin插件

### 调用参数
`connect`调用的参数为要连接的eos节点旳地址，字符串

### 返回值
...

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://127.0.0.1:8888/v1/net/connect -d 1.2.3.4:9876
```

返回结果：
```json
{
    ...
}
```

