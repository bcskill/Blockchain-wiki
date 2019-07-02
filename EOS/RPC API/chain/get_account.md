# chain/get_account

`chain/get_account`调用返回指定账号的描述信息

注意，nodeos时需要启用chain_api_plugin插件

### 调用参数
JSON对象，用来指定要读取信息的账号，其成员如下：

- account_name：账号名称，字符串

### 返回值
`get_account`调用的返回值是描述账号信息的JSON对象，其成员如下：

- account_name：账号名称
- permissions: 账号权限集合，权限对象数组，每个权限对象的成员如下：
  - perm_name：权限名称
  - parent：父权限名称
  - required_auth：授权条件，JSON对象，成员如下：
    - threshold：阈值，整数
    - keys：公钥信息集合，数组，每个公钥信息对象成员如下：
      - key：公钥，字符串
      - weight：权重
      - accounts：账号数组

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/chain/get_account -d '{
  "account_name": "bcskillsurou"
}'
```

返回结果：
```json
{
    "account_name":"bcskillsurou",
    "head_block_num":66519357,
    "head_block_time":"2019-07-02T06:39:15.000",
    "privileged":false,
    "last_code_update":"1970-01-01T00:00:00.000",
    "created":"2018-06-25T10:39:42.000",
    "core_liquid_balance":"0.1037 EOS",
    "ram_quota":4452,
    "net_weight":46,
    "cpu_weight":147,
    "net_limit":{
        "used":736,
        "available":3530,
        "max":4266
    },
    "cpu_limit":{
        "used":1852,
        "available":606,
        "max":2458
    },
    "ram_usage":3574,
    "permissions":[
        {
            "perm_name":"active",
            "parent":"owner",
            "required_auth":{
                "threshold":1,
                "keys":[
                    {
                        "key":"EOS77QxpZtsEj6v2FviNP3NY1LEy4UndZDs385jfJ6Hf8uvPpJbsk",
                        "weight":1
                    }
                ],
                "accounts":[

                ],
                "waits":[

                ]
            }
        },
        {
            "perm_name":"owner",
            "parent":"",
            "required_auth":{
                "threshold":1,
                "keys":[
                    {
                        "key":"EOS6M4ag92kgXj2F3MNNyVP1TiKXkDRkpMaqA5izbCH5CjUovuRzb",
                        "weight":1
                    }
                ],
                "accounts":[

                ],
                "waits":[

                ]
            }
        }
    ],
    "total_resources":{
        "owner":"bcskillsurou",
        "net_weight":"0.0046 EOS",
        "cpu_weight":"0.0147 EOS",
        "ram_bytes":3052
    },
    "self_delegated_bandwidth":{
        "from":"bcskillsurou",
        "to":"bcskillsurou",
        "net_weight":"0.0046 EOS",
        "cpu_weight":"0.0147 EOS"
    },
    "refund_request":null,
    "voter_info":{
        "owner":"bcskillsurou",
        "proxy":"",
        "producers":[

        ],
        "staked":193,
        "last_vote_weight":"0.00000000000000000",
        "proxied_vote_weight":"0.00000000000000000",
        "is_proxy":0,
        "flags1":0,
        "reserved2":0,
        "reserved3":"0 "
    }
}
```