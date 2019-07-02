# history/get_controlled_accounts

`history/get_controlled_accounts`调用返回指定账号的受控账号。

注意，nodeos时需要启用history_api_plugin插件，并且设置filter-on选项

### 调用参数
JSON对象，声明主控账号，其成员为：

- controlling_account：主控账号名称，字符串

### 返回值
`get_controlled_accounts`调用返回一组受控账号

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/history/get_controlled_accounts -d '{
  "controlling_account":"eosio"
}'
```

返回结果：
```json
{
    "controlled_accounts":[
        "decentwitter",
        "eoshappyvote",
        "eosio.bpay",
        "eosio.forum",
        "eosio.lost",
        "eosio.msig",
        "eosio.names",
        "eosio.ram",
        "eosio.ramfee",
        "eosio.regram",
        "eosio.rex",
        "eosio.saving",
        "eosio.stake",
        "eosio.token",
        "eosio.unregd",
        "eosio.vpay",
        "eosio.wrap",
        "eoslocktoken",
        "eosvrmarkets",
        "eosvrrewards",
        "eosvrtokenss",
        "evdadvancer1",
        "evdadvancers",
        "evdpopulariz",
        "evradvancer1",
        "evradvancers",
        "evrportraits",
        "freewithdraw",
        "frogfrogcoin",
        "gm2dimrqgige",
        "nvoyiooiyovn",
        "ssssssss1115",
        "stoponnopots",
        "testtodelete",
        "toohottohoot",
        "unusedaccnts"
    ]
}
```



### 参考

https://www.bcskill.com/index.php/archives/619.html