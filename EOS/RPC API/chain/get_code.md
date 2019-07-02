# chain/get_code

`chain/get_code`调用返回指定账号所托管合约的代码信息

注意，nodeos时需要启用chain_api_plugin插件

### 调用参数
JSON对象，用来声明要查询代码的账号，其成员如下：

- account_name：账号名称，字符串

### 返回值
`get_code`调用返回指定账号上部署的合约的代码描述对象，其成员如下：

- name：账号名称，字符串
- code_hash：当前部署代码的哈希值，字符串
- wast：当前部署代码的等价文本格式，字符串
- abi：当前部署代码的abi描述对象，其成员如下：
  - types：abi中定义的新类型，数组
  - structs：abi中定义的新结构，数组
  - actions：abi中定义的合约动作，数组
  - tables：abi中定义的数据表，数组

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/chain/get_code -d '{
  "account_name": "bcskillsurou"
}'
```

返回结果：
```json
{
  "name":"bcskillsurou",
  "code_hash":"a1c8c84b4700c09c8edb83522237439e33cf011a4d7ace51075998bd002e04c9",
  "wast":"(module\n  (type $0 (func (param i64 i64 i32) (result i32)))\n ...truncated",
  "abi": {
  "types": [{
      "new_type_name": "account_name",
      "type": "name"
    }
  ],
  "structs": [{
      "name": "transfer",
      "base": "",
      "fields": [
        {"name":"from", "type":"account_name"},
        {"name":"to", "type":"account_name"},
        {"name":"quantity", "type":"uint64"}
      ]
    },{
      "name": "account",
      "base": "",
      "fields": [
        {"name":"key", "type":"name"},
        {"name":"balance", "type":"uint64"}
      ]
    }
  ],
  "actions": [{
      "name": "transfer",
      "type": "transfer"
    }
  ],
  "tables": [{
      "name": "account",
      "type": "account",
      "index_type": "i64",
      "key_names" : ["key"],
      "key_types" : ["name"]
    }
  ]
}
```

### 参考

### [Returning WAST from get_code is no longer supported](https://www.bcskill.com/index.php/archives/496.html)