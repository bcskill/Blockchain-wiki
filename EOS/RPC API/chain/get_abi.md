# chain/get_abi

`chain/get_abi`调用返回指定账号所托管合约的abi描述信息

注意，nodeos时需要启用chain_api_plugin插件

### 调用参数
JSON对象，用来指定要查询的合约托管账户，其成员如下：

- account_name：账户名称，字符串

### 返回值
`get_abi`调用返回指定账号上所部署的合约的abi描述对象。

### 示例代码
调用请求：
```shell
~$ curl -X POST --url https://api.eoslaomao.com/v1/chain/get_abi -d '{
  "account_name": "eosio"
}'
```

返回结果：
```json
{
    "account_name":"eosio",
    "abi":{
        "version":"eosio::abi/1.1",
        "types":[

        ],
        "structs":[
            {
                "name":"abi_hash",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"hash",
                        "type":"checksum256"
                    }
                ]
            },
            {
                "name":"authority",
                "base":"",
                "fields":[
                    {
                        "name":"threshold",
                        "type":"uint32"
                    },
                    {
                        "name":"keys",
                        "type":"key_weight[]"
                    },
                    {
                        "name":"accounts",
                        "type":"permission_level_weight[]"
                    },
                    {
                        "name":"waits",
                        "type":"wait_weight[]"
                    }
                ]
            },
            {
                "name":"bid_refund",
                "base":"",
                "fields":[
                    {
                        "name":"bidder",
                        "type":"name"
                    },
                    {
                        "name":"amount",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"bidname",
                "base":"",
                "fields":[
                    {
                        "name":"bidder",
                        "type":"name"
                    },
                    {
                        "name":"newname",
                        "type":"name"
                    },
                    {
                        "name":"bid",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"bidrefund",
                "base":"",
                "fields":[
                    {
                        "name":"bidder",
                        "type":"name"
                    },
                    {
                        "name":"newname",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"block_header",
                "base":"",
                "fields":[
                    {
                        "name":"timestamp",
                        "type":"uint32"
                    },
                    {
                        "name":"producer",
                        "type":"name"
                    },
                    {
                        "name":"confirmed",
                        "type":"uint16"
                    },
                    {
                        "name":"previous",
                        "type":"checksum256"
                    },
                    {
                        "name":"transaction_mroot",
                        "type":"checksum256"
                    },
                    {
                        "name":"action_mroot",
                        "type":"checksum256"
                    },
                    {
                        "name":"schedule_version",
                        "type":"uint32"
                    },
                    {
                        "name":"new_producers",
                        "type":"producer_schedule?"
                    }
                ]
            },
            {
                "name":"blockchain_parameters",
                "base":"",
                "fields":[
                    {
                        "name":"max_block_net_usage",
                        "type":"uint64"
                    },
                    {
                        "name":"target_block_net_usage_pct",
                        "type":"uint32"
                    },
                    {
                        "name":"max_transaction_net_usage",
                        "type":"uint32"
                    },
                    {
                        "name":"base_per_transaction_net_usage",
                        "type":"uint32"
                    },
                    {
                        "name":"net_usage_leeway",
                        "type":"uint32"
                    },
                    {
                        "name":"context_free_discount_net_usage_num",
                        "type":"uint32"
                    },
                    {
                        "name":"context_free_discount_net_usage_den",
                        "type":"uint32"
                    },
                    {
                        "name":"max_block_cpu_usage",
                        "type":"uint32"
                    },
                    {
                        "name":"target_block_cpu_usage_pct",
                        "type":"uint32"
                    },
                    {
                        "name":"max_transaction_cpu_usage",
                        "type":"uint32"
                    },
                    {
                        "name":"min_transaction_cpu_usage",
                        "type":"uint32"
                    },
                    {
                        "name":"max_transaction_lifetime",
                        "type":"uint32"
                    },
                    {
                        "name":"deferred_trx_expiration_window",
                        "type":"uint32"
                    },
                    {
                        "name":"max_transaction_delay",
                        "type":"uint32"
                    },
                    {
                        "name":"max_inline_action_size",
                        "type":"uint32"
                    },
                    {
                        "name":"max_inline_action_depth",
                        "type":"uint16"
                    },
                    {
                        "name":"max_authority_depth",
                        "type":"uint16"
                    }
                ]
            },
            {
                "name":"buyram",
                "base":"",
                "fields":[
                    {
                        "name":"payer",
                        "type":"name"
                    },
                    {
                        "name":"receiver",
                        "type":"name"
                    },
                    {
                        "name":"quant",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"buyrambytes",
                "base":"",
                "fields":[
                    {
                        "name":"payer",
                        "type":"name"
                    },
                    {
                        "name":"receiver",
                        "type":"name"
                    },
                    {
                        "name":"bytes",
                        "type":"uint32"
                    }
                ]
            },
            {
                "name":"buyrex",
                "base":"",
                "fields":[
                    {
                        "name":"from",
                        "type":"name"
                    },
                    {
                        "name":"amount",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"canceldelay",
                "base":"",
                "fields":[
                    {
                        "name":"canceling_auth",
                        "type":"permission_level"
                    },
                    {
                        "name":"trx_id",
                        "type":"checksum256"
                    }
                ]
            },
            {
                "name":"claimrewards",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"closerex",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"cnclrexorder",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"connector",
                "base":"",
                "fields":[
                    {
                        "name":"balance",
                        "type":"asset"
                    },
                    {
                        "name":"weight",
                        "type":"float64"
                    }
                ]
            },
            {
                "name":"consolidate",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"defcpuloan",
                "base":"",
                "fields":[
                    {
                        "name":"from",
                        "type":"name"
                    },
                    {
                        "name":"loan_num",
                        "type":"uint64"
                    },
                    {
                        "name":"amount",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"defnetloan",
                "base":"",
                "fields":[
                    {
                        "name":"from",
                        "type":"name"
                    },
                    {
                        "name":"loan_num",
                        "type":"uint64"
                    },
                    {
                        "name":"amount",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"delegatebw",
                "base":"",
                "fields":[
                    {
                        "name":"from",
                        "type":"name"
                    },
                    {
                        "name":"receiver",
                        "type":"name"
                    },
                    {
                        "name":"stake_net_quantity",
                        "type":"asset"
                    },
                    {
                        "name":"stake_cpu_quantity",
                        "type":"asset"
                    },
                    {
                        "name":"transfer",
                        "type":"bool"
                    }
                ]
            },
            {
                "name":"delegated_bandwidth",
                "base":"",
                "fields":[
                    {
                        "name":"from",
                        "type":"name"
                    },
                    {
                        "name":"to",
                        "type":"name"
                    },
                    {
                        "name":"net_weight",
                        "type":"asset"
                    },
                    {
                        "name":"cpu_weight",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"deleteauth",
                "base":"",
                "fields":[
                    {
                        "name":"account",
                        "type":"name"
                    },
                    {
                        "name":"permission",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"deposit",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"amount",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"eosio_global_state",
                "base":"blockchain_parameters",
                "fields":[
                    {
                        "name":"max_ram_size",
                        "type":"uint64"
                    },
                    {
                        "name":"total_ram_bytes_reserved",
                        "type":"uint64"
                    },
                    {
                        "name":"total_ram_stake",
                        "type":"int64"
                    },
                    {
                        "name":"last_producer_schedule_update",
                        "type":"block_timestamp_type"
                    },
                    {
                        "name":"last_pervote_bucket_fill",
                        "type":"time_point"
                    },
                    {
                        "name":"pervote_bucket",
                        "type":"int64"
                    },
                    {
                        "name":"perblock_bucket",
                        "type":"int64"
                    },
                    {
                        "name":"total_unpaid_blocks",
                        "type":"uint32"
                    },
                    {
                        "name":"total_activated_stake",
                        "type":"int64"
                    },
                    {
                        "name":"thresh_activated_stake_time",
                        "type":"time_point"
                    },
                    {
                        "name":"last_producer_schedule_size",
                        "type":"uint16"
                    },
                    {
                        "name":"total_producer_vote_weight",
                        "type":"float64"
                    },
                    {
                        "name":"last_name_close",
                        "type":"block_timestamp_type"
                    }
                ]
            },
            {
                "name":"eosio_global_state2",
                "base":"",
                "fields":[
                    {
                        "name":"new_ram_per_block",
                        "type":"uint16"
                    },
                    {
                        "name":"last_ram_increase",
                        "type":"block_timestamp_type"
                    },
                    {
                        "name":"last_block_num",
                        "type":"block_timestamp_type"
                    },
                    {
                        "name":"total_producer_votepay_share",
                        "type":"float64"
                    },
                    {
                        "name":"revision",
                        "type":"uint8"
                    }
                ]
            },
            {
                "name":"eosio_global_state3",
                "base":"",
                "fields":[
                    {
                        "name":"last_vpay_state_update",
                        "type":"time_point"
                    },
                    {
                        "name":"total_vpay_share_change_rate",
                        "type":"float64"
                    }
                ]
            },
            {
                "name":"exchange_state",
                "base":"",
                "fields":[
                    {
                        "name":"supply",
                        "type":"asset"
                    },
                    {
                        "name":"base",
                        "type":"connector"
                    },
                    {
                        "name":"quote",
                        "type":"connector"
                    }
                ]
            },
            {
                "name":"fundcpuloan",
                "base":"",
                "fields":[
                    {
                        "name":"from",
                        "type":"name"
                    },
                    {
                        "name":"loan_num",
                        "type":"uint64"
                    },
                    {
                        "name":"payment",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"fundnetloan",
                "base":"",
                "fields":[
                    {
                        "name":"from",
                        "type":"name"
                    },
                    {
                        "name":"loan_num",
                        "type":"uint64"
                    },
                    {
                        "name":"payment",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"init",
                "base":"",
                "fields":[
                    {
                        "name":"version",
                        "type":"varuint32"
                    },
                    {
                        "name":"core",
                        "type":"symbol"
                    }
                ]
            },
            {
                "name":"key_weight",
                "base":"",
                "fields":[
                    {
                        "name":"key",
                        "type":"public_key"
                    },
                    {
                        "name":"weight",
                        "type":"uint16"
                    }
                ]
            },
            {
                "name":"linkauth",
                "base":"",
                "fields":[
                    {
                        "name":"account",
                        "type":"name"
                    },
                    {
                        "name":"code",
                        "type":"name"
                    },
                    {
                        "name":"type",
                        "type":"name"
                    },
                    {
                        "name":"requirement",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"mvfrsavings",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"rex",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"mvtosavings",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"rex",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"name_bid",
                "base":"",
                "fields":[
                    {
                        "name":"newname",
                        "type":"name"
                    },
                    {
                        "name":"high_bidder",
                        "type":"name"
                    },
                    {
                        "name":"high_bid",
                        "type":"int64"
                    },
                    {
                        "name":"last_bid_time",
                        "type":"time_point"
                    }
                ]
            },
            {
                "name":"newaccount",
                "base":"",
                "fields":[
                    {
                        "name":"creator",
                        "type":"name"
                    },
                    {
                        "name":"name",
                        "type":"name"
                    },
                    {
                        "name":"owner",
                        "type":"authority"
                    },
                    {
                        "name":"active",
                        "type":"authority"
                    }
                ]
            },
            {
                "name":"onblock",
                "base":"",
                "fields":[
                    {
                        "name":"header",
                        "type":"block_header"
                    }
                ]
            },
            {
                "name":"onerror",
                "base":"",
                "fields":[
                    {
                        "name":"sender_id",
                        "type":"uint128"
                    },
                    {
                        "name":"sent_trx",
                        "type":"bytes"
                    }
                ]
            },
            {
                "name":"pair_time_point_sec_int64",
                "base":"",
                "fields":[
                    {
                        "name":"first",
                        "type":"time_point_sec"
                    },
                    {
                        "name":"second",
                        "type":"int64"
                    }
                ]
            },
            {
                "name":"permission_level",
                "base":"",
                "fields":[
                    {
                        "name":"actor",
                        "type":"name"
                    },
                    {
                        "name":"permission",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"permission_level_weight",
                "base":"",
                "fields":[
                    {
                        "name":"permission",
                        "type":"permission_level"
                    },
                    {
                        "name":"weight",
                        "type":"uint16"
                    }
                ]
            },
            {
                "name":"producer_info",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"total_votes",
                        "type":"float64"
                    },
                    {
                        "name":"producer_key",
                        "type":"public_key"
                    },
                    {
                        "name":"is_active",
                        "type":"bool"
                    },
                    {
                        "name":"url",
                        "type":"string"
                    },
                    {
                        "name":"unpaid_blocks",
                        "type":"uint32"
                    },
                    {
                        "name":"last_claim_time",
                        "type":"time_point"
                    },
                    {
                        "name":"location",
                        "type":"uint16"
                    }
                ]
            },
            {
                "name":"producer_info2",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"votepay_share",
                        "type":"float64"
                    },
                    {
                        "name":"last_votepay_share_update",
                        "type":"time_point"
                    }
                ]
            },
            {
                "name":"producer_key",
                "base":"",
                "fields":[
                    {
                        "name":"producer_name",
                        "type":"name"
                    },
                    {
                        "name":"block_signing_key",
                        "type":"public_key"
                    }
                ]
            },
            {
                "name":"producer_schedule",
                "base":"",
                "fields":[
                    {
                        "name":"version",
                        "type":"uint32"
                    },
                    {
                        "name":"producers",
                        "type":"producer_key[]"
                    }
                ]
            },
            {
                "name":"refund",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"refund_request",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"request_time",
                        "type":"time_point_sec"
                    },
                    {
                        "name":"net_amount",
                        "type":"asset"
                    },
                    {
                        "name":"cpu_amount",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"regproducer",
                "base":"",
                "fields":[
                    {
                        "name":"producer",
                        "type":"name"
                    },
                    {
                        "name":"producer_key",
                        "type":"public_key"
                    },
                    {
                        "name":"url",
                        "type":"string"
                    },
                    {
                        "name":"location",
                        "type":"uint16"
                    }
                ]
            },
            {
                "name":"regproxy",
                "base":"",
                "fields":[
                    {
                        "name":"proxy",
                        "type":"name"
                    },
                    {
                        "name":"isproxy",
                        "type":"bool"
                    }
                ]
            },
            {
                "name":"rentcpu",
                "base":"",
                "fields":[
                    {
                        "name":"from",
                        "type":"name"
                    },
                    {
                        "name":"receiver",
                        "type":"name"
                    },
                    {
                        "name":"loan_payment",
                        "type":"asset"
                    },
                    {
                        "name":"loan_fund",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"rentnet",
                "base":"",
                "fields":[
                    {
                        "name":"from",
                        "type":"name"
                    },
                    {
                        "name":"receiver",
                        "type":"name"
                    },
                    {
                        "name":"loan_payment",
                        "type":"asset"
                    },
                    {
                        "name":"loan_fund",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"rex_balance",
                "base":"",
                "fields":[
                    {
                        "name":"version",
                        "type":"uint8"
                    },
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"vote_stake",
                        "type":"asset"
                    },
                    {
                        "name":"rex_balance",
                        "type":"asset"
                    },
                    {
                        "name":"matured_rex",
                        "type":"int64"
                    },
                    {
                        "name":"rex_maturities",
                        "type":"pair_time_point_sec_int64[]"
                    }
                ]
            },
            {
                "name":"rex_fund",
                "base":"",
                "fields":[
                    {
                        "name":"version",
                        "type":"uint8"
                    },
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"balance",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"rex_loan",
                "base":"",
                "fields":[
                    {
                        "name":"version",
                        "type":"uint8"
                    },
                    {
                        "name":"from",
                        "type":"name"
                    },
                    {
                        "name":"receiver",
                        "type":"name"
                    },
                    {
                        "name":"payment",
                        "type":"asset"
                    },
                    {
                        "name":"balance",
                        "type":"asset"
                    },
                    {
                        "name":"total_staked",
                        "type":"asset"
                    },
                    {
                        "name":"loan_num",
                        "type":"uint64"
                    },
                    {
                        "name":"expiration",
                        "type":"time_point"
                    }
                ]
            },
            {
                "name":"rex_order",
                "base":"",
                "fields":[
                    {
                        "name":"version",
                        "type":"uint8"
                    },
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"rex_requested",
                        "type":"asset"
                    },
                    {
                        "name":"proceeds",
                        "type":"asset"
                    },
                    {
                        "name":"stake_change",
                        "type":"asset"
                    },
                    {
                        "name":"order_time",
                        "type":"time_point"
                    },
                    {
                        "name":"is_open",
                        "type":"bool"
                    }
                ]
            },
            {
                "name":"rex_pool",
                "base":"",
                "fields":[
                    {
                        "name":"version",
                        "type":"uint8"
                    },
                    {
                        "name":"total_lent",
                        "type":"asset"
                    },
                    {
                        "name":"total_unlent",
                        "type":"asset"
                    },
                    {
                        "name":"total_rent",
                        "type":"asset"
                    },
                    {
                        "name":"total_lendable",
                        "type":"asset"
                    },
                    {
                        "name":"total_rex",
                        "type":"asset"
                    },
                    {
                        "name":"namebid_proceeds",
                        "type":"asset"
                    },
                    {
                        "name":"loan_num",
                        "type":"uint64"
                    }
                ]
            },
            {
                "name":"rexexec",
                "base":"",
                "fields":[
                    {
                        "name":"user",
                        "type":"name"
                    },
                    {
                        "name":"max",
                        "type":"uint16"
                    }
                ]
            },
            {
                "name":"rmvproducer",
                "base":"",
                "fields":[
                    {
                        "name":"producer",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"sellram",
                "base":"",
                "fields":[
                    {
                        "name":"account",
                        "type":"name"
                    },
                    {
                        "name":"bytes",
                        "type":"int64"
                    }
                ]
            },
            {
                "name":"sellrex",
                "base":"",
                "fields":[
                    {
                        "name":"from",
                        "type":"name"
                    },
                    {
                        "name":"rex",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"setabi",
                "base":"",
                "fields":[
                    {
                        "name":"account",
                        "type":"name"
                    },
                    {
                        "name":"abi",
                        "type":"bytes"
                    }
                ]
            },
            {
                "name":"setacctcpu",
                "base":"",
                "fields":[
                    {
                        "name":"account",
                        "type":"name"
                    },
                    {
                        "name":"cpu_weight",
                        "type":"int64?"
                    }
                ]
            },
            {
                "name":"setacctnet",
                "base":"",
                "fields":[
                    {
                        "name":"account",
                        "type":"name"
                    },
                    {
                        "name":"net_weight",
                        "type":"int64?"
                    }
                ]
            },
            {
                "name":"setacctram",
                "base":"",
                "fields":[
                    {
                        "name":"account",
                        "type":"name"
                    },
                    {
                        "name":"ram_bytes",
                        "type":"int64?"
                    }
                ]
            },
            {
                "name":"setalimits",
                "base":"",
                "fields":[
                    {
                        "name":"account",
                        "type":"name"
                    },
                    {
                        "name":"ram_bytes",
                        "type":"int64"
                    },
                    {
                        "name":"net_weight",
                        "type":"int64"
                    },
                    {
                        "name":"cpu_weight",
                        "type":"int64"
                    }
                ]
            },
            {
                "name":"setcode",
                "base":"",
                "fields":[
                    {
                        "name":"account",
                        "type":"name"
                    },
                    {
                        "name":"vmtype",
                        "type":"uint8"
                    },
                    {
                        "name":"vmversion",
                        "type":"uint8"
                    },
                    {
                        "name":"code",
                        "type":"bytes"
                    }
                ]
            },
            {
                "name":"setparams",
                "base":"",
                "fields":[
                    {
                        "name":"params",
                        "type":"blockchain_parameters"
                    }
                ]
            },
            {
                "name":"setpriv",
                "base":"",
                "fields":[
                    {
                        "name":"account",
                        "type":"name"
                    },
                    {
                        "name":"is_priv",
                        "type":"uint8"
                    }
                ]
            },
            {
                "name":"setram",
                "base":"",
                "fields":[
                    {
                        "name":"max_ram_size",
                        "type":"uint64"
                    }
                ]
            },
            {
                "name":"setramrate",
                "base":"",
                "fields":[
                    {
                        "name":"bytes_per_block",
                        "type":"uint16"
                    }
                ]
            },
            {
                "name":"setrex",
                "base":"",
                "fields":[
                    {
                        "name":"balance",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"undelegatebw",
                "base":"",
                "fields":[
                    {
                        "name":"from",
                        "type":"name"
                    },
                    {
                        "name":"receiver",
                        "type":"name"
                    },
                    {
                        "name":"unstake_net_quantity",
                        "type":"asset"
                    },
                    {
                        "name":"unstake_cpu_quantity",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"unlinkauth",
                "base":"",
                "fields":[
                    {
                        "name":"account",
                        "type":"name"
                    },
                    {
                        "name":"code",
                        "type":"name"
                    },
                    {
                        "name":"type",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"unregprod",
                "base":"",
                "fields":[
                    {
                        "name":"producer",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"unstaketorex",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"receiver",
                        "type":"name"
                    },
                    {
                        "name":"from_net",
                        "type":"asset"
                    },
                    {
                        "name":"from_cpu",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"updateauth",
                "base":"",
                "fields":[
                    {
                        "name":"account",
                        "type":"name"
                    },
                    {
                        "name":"permission",
                        "type":"name"
                    },
                    {
                        "name":"parent",
                        "type":"name"
                    },
                    {
                        "name":"auth",
                        "type":"authority"
                    }
                ]
            },
            {
                "name":"updaterex",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    }
                ]
            },
            {
                "name":"updtrevision",
                "base":"",
                "fields":[
                    {
                        "name":"revision",
                        "type":"uint8"
                    }
                ]
            },
            {
                "name":"user_resources",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"net_weight",
                        "type":"asset"
                    },
                    {
                        "name":"cpu_weight",
                        "type":"asset"
                    },
                    {
                        "name":"ram_bytes",
                        "type":"int64"
                    }
                ]
            },
            {
                "name":"voteproducer",
                "base":"",
                "fields":[
                    {
                        "name":"voter",
                        "type":"name"
                    },
                    {
                        "name":"proxy",
                        "type":"name"
                    },
                    {
                        "name":"producers",
                        "type":"name[]"
                    }
                ]
            },
            {
                "name":"voter_info",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"proxy",
                        "type":"name"
                    },
                    {
                        "name":"producers",
                        "type":"name[]"
                    },
                    {
                        "name":"staked",
                        "type":"int64"
                    },
                    {
                        "name":"last_vote_weight",
                        "type":"float64"
                    },
                    {
                        "name":"proxied_vote_weight",
                        "type":"float64"
                    },
                    {
                        "name":"is_proxy",
                        "type":"bool"
                    },
                    {
                        "name":"flags1",
                        "type":"uint32"
                    },
                    {
                        "name":"reserved2",
                        "type":"uint32"
                    },
                    {
                        "name":"reserved3",
                        "type":"asset"
                    }
                ]
            },
            {
                "name":"wait_weight",
                "base":"",
                "fields":[
                    {
                        "name":"wait_sec",
                        "type":"uint32"
                    },
                    {
                        "name":"weight",
                        "type":"uint16"
                    }
                ]
            },
            {
                "name":"withdraw",
                "base":"",
                "fields":[
                    {
                        "name":"owner",
                        "type":"name"
                    },
                    {
                        "name":"amount",
                        "type":"asset"
                    }
                ]
            }
        ],
        "actions":[
            {
                "name":"bidname",
                "type":"bidname",
                "ricardian_contract":"# Action - `{{ bidname }}`

## Description

The `{{ bidname }}` action places a bid on a premium account name, in the knowledge that the high bid will purchase the name.

As an authorized party I {{ signer }} wish to bid on behalf of {{ bidder }} the amount of {{ bid }} toward purchase of the account name {{ newname }}.
"
            },
            {
                "name":"bidrefund",
                "type":"bidrefund",
                "ricardian_contract":""
            },
            {
                "name":"buyram",
                "type":"buyram",
                "ricardian_contract":"# Action - `{{ buyram }}`

### Description

This action will attempt to reserve about {{quant}} worth of RAM on behalf of {{receiver}}. 

{{buyer}} authorizes this contract to transfer {{quant}} to buy RAM based upon the current price as determined by the market maker algorithm.

{{buyer}} accepts that a 0.5% fee will be charged on the amount spent and that the actual RAM received may be slightly less than expected due to the approximations necessary to enable this service.
{{buyer}} accepts that a 0.5% fee will be charged if and when they sell the RAM received.
{{buyer}} accepts that rounding errors resulting from limits of computational precision may result in less RAM being allocated.
{{buyer}} acknowledges that the supply of RAM may be increased at any time up to the limits of off-the-shelf computer equipment and that this may result in RAM selling for less than purchase price.
{{buyer}} acknowledges that the price of RAM may increase or decrease over time according to supply and demand.
{{buyer}} acknowledges that RAM is non-transferrable. 
{{buyer}} acknowledges RAM currently in use by their account cannot be sold until it is freed and that freeing RAM may be subject to terms of other contracts.

"
            },
            {
                "name":"buyrambytes",
                "type":"buyrambytes",
                "ricardian_contract":"# Action - `{{ buyrambytes }}`

### Description

This action will attempt to reserve about {{bytes}} bytes of RAM on behalf of {{receiver}}. 

{{buyer}} authorizes this contract to transfer sufficient EOS tokens to buy the RAM based upon the current price as determined by the market maker algorithm.

{{buyer}} accepts that a 0.5% fee will be charged on the EOS spent and that the actual RAM received may be slightly less than requested due to the approximations necessary to enable this service.
{{buyer}} accepts that a 0.5% fee will be charged if and when they sell the RAM received.
{{buyer}} accepts that rounding errors resulting from limits of computational precision may result in less RAM being allocated.
{{buyer}} acknowledges that the supply of RAM may be increased at any time up to the limits of off-the-shelf computer equipment and that this may result in RAM selling for less than purchase price.
{{buyer}} acknowledges that the price of RAM may increase or decrease over time according to supply and demand.
{{buyer}} acknowledges that RAM is non-transferable. 
{{buyer}} acknowledges RAM currently in use by their account cannot be sold until it is freed and that freeing RAM may be subject to terms of other contracts.

"
            },
            {
                "name":"buyrex",
                "type":"buyrex",
                "ricardian_contract":"# Action - `buyrex`

## Description

The `buyrex` action allows an account to buy REX in exchange for tokens taken out of the user's REX fund.

As an authorized party I {{ signer }} wish to buy REX on the account {{ from }} with the amount {{ amount }} EOS.

I am aware of, and have fulfilled, all voting requirements needed to participate in the REX marketplace.
"
            },
            {
                "name":"canceldelay",
                "type":"canceldelay",
                "ricardian_contract":"# Action - `{{ canceldelay }}`

### Description

The `{{ canceldelay }}` action cancels an existing delayed transaction.

As an authorized party I {{ signer }} wish to invoke the authority of {{ canceling_auth }} to cancel the transaction with ID {{ trx_id }}.
"
            },
            {
                "name":"claimrewards",
                "type":"claimrewards",
                "ricardian_contract":"# Action - `{{ claimrewards }}`

## Description

The `{{ claimrewards }}` action allows a block producer (active or standby) to claim the system rewards due them for producing blocks and receiving votes.

As an authorized party I {{ signer }} wish to have the rewards earned by {{ owner }} deposited into the {{ owner }} account.
"
            },
            {
                "name":"closerex",
                "type":"closerex",
                "ricardian_contract":"# Action - `closerex`

## Description

The `closerex` action allows an account to delete unused REX-related database entries and frees occupied RAM associated with its storage.

As an authorized party, I {{ signer }}, wish to delete all unused REX-related database entries from the account {{ owner }}.

I will not be able to succesfully call `closerex` unless all checks for CPU loans, NET loans or refunds pending refunds are still processing on the account {{ owner }}.
"
            },
            {
                "name":"cnclrexorder",
                "type":"cnclrexorder",
                "ricardian_contract":"# Action - `cnclrexorder`

## Description

The `cnclrexorder` action cancels a queued REX sell order if one exists for an account.

As an authorized party I, {{ signer }}, wish to cancel any unfilled and queued REX sell orders that exist for the account {{ owner }}. 
"
            },
            {
                "name":"consolidate",
                "type":"consolidate",
                "ricardian_contract":" # Action - `consolidate`

## Description

The `consolidate` action will consolidate all REX maturity buckets for an account into one that matures 4 days from 00:00 UTC.

As an authorized party I, {{ signer }}, wish to consolidate any open REX maturity buckets for the account {{ owner }} into one that matures 4 days from the following 00:00 UTC.
"
            },
            {
                "name":"defcpuloan",
                "type":"defcpuloan",
                "ricardian_contract":"# Action - `defcpuloan`

## Description

The `defcpuloan` action allows an account to withdraw tokens from the fund of a specific CPU loan and adds them to REX fund.

As an authorized party I, {{ signer }}, wish to withdraw from the CPU loan fund identified by loan number {{ loan_num }} on the account {{ from }} in the amount of {{ amount }} and have those tokens allocated to the REX fund of {{ from }}.
"
            },
            {
                "name":"defnetloan",
                "type":"defnetloan",
                "ricardian_contract":"# Action - `defnetloan`

## Description

The `defnetloan` action allows an account to withdraw tokens from the fund of a specific Network loan and adds them to REX fund.

As an authorized party I, {{ signer }}, wish to withdraw from the Network loan fund identified by loan number {{ loan_num }} on the account {{ from }} in the amount of {{ amount }} and have those tokens allocated to the REX fund of {{ from }}.
"
            },
            {
                "name":"delegatebw",
                "type":"delegatebw",
                "ricardian_contract":"# Action - `{{ delegatebw }}`

## Description

The intent of the `{{ delegatebw }}` action is to stake tokens for bandwidth and/or CPU and optionally transfer ownership.

As an authorized party I {{ signer }} wish to stake {{ stake_cpu_quantity }} for CPU and {{ stake_net_quantity }} for bandwidth from the liquid tokens of {{ from }} for the use of delegatee {{ to }}. 

{{if transfer }}

It is {{ transfer }} that I wish these tokens to become immediately owned by the delegatee.

{{/if}}

As signer I stipulate that, if I am not the beneficial owner of these tokens, I have proof that Iu2019ve been authorized to take this action by their beneficial owner(s). 
"
            },
            {
                "name":"deleteauth",
                "type":"deleteauth",
                "ricardian_contract":""
            },
            {
                "name":"deposit",
                "type":"deposit",
                "ricardian_contract":"# Action - `deposit`

## Description

The `deposit` action allows an account to deposit EOS tokens into REX fund by transfering from their liquid token balance.

As an authorized party I, {{ signer }}, wish to deposit {{ amount }} EOS tokens into the REX fund of the account {{ owner }} from the liquid token balance of {{ owner }}.
"
            },
            {
                "name":"fundcpuloan",
                "type":"fundcpuloan",
                "ricardian_contract":"# Action - `fundcpuloan`

## Description

The `fundcpuloan` action allows an account to transfer tokens from its REX fund to the fund of a specific CPU loan in order for those tokens to be used for loan renewal at the loan's expiry.

As an authorized party I, {{ signer }}, wish to transfer the amount of {{ payment }} tokens into the CPU loan fund of the loan identified by loan number {{ loan_num }} from the account {{ from }} to be used for loan renewal at the expiry of {{ loan_num }}.
"
            },
            {
                "name":"fundnetloan",
                "type":"fundnetloan",
                "ricardian_contract":"# Action - `fundnetloan`

## Description

The `fundnetloan` action allows an account to transfer tokens from its REX fund to the fund of a specific Network loan in order for those tokens to be used for loan renewal at the loan's expiry.

As an authorized party I, {{ signer }}, wish to transfer the amount of {{ payment }} tokens into the Network loan fund of the loan identified by loan number {{ loan_num }} from the account {{ from }} to be used for loan renewal at the expiry of {{ loan_num }}.
"
            },
            {
                "name":"init",
                "type":"init",
                "ricardian_contract":""
            },
            {
                "name":"linkauth",
                "type":"linkauth",
                "ricardian_contract":""
            },
            {
                "name":"mvfrsavings",
                "type":"mvfrsavings",
                "ricardian_contract":"# Action - `mvfrsavings`

## Description

The `mvfrsavings` action allows an account to move REX tokens from its savings bucket to a bucket with a maturity date that is 4 days after 00:00 UTC.

As an authorized party I, {{ signer }}, wish to move {{ rex }} tokens from the savings bucket of the account {{ owner }}. Those tokens shall become available to {{ owner }} 4 days from 00:00 UTC.
"
            },
            {
                "name":"mvtosavings",
                "type":"mvtosavings",
                "ricardian_contract":"# Action - `mvtosavings`

## Description

The `mvtosavings` action allows an account to move REX tokens into a savings bucket.

As an authorized party I, {{ signer }}, wish to move {{ rex }} tokens to a savings bucket associated to the account {{ owner }}. I acknowledge that those tokens will then be subject to any maturity restrictions described in the `mvfrsavings` action. 
"
            },
            {
                "name":"newaccount",
                "type":"newaccount",
                "ricardian_contract":"# Action - `{{ newaccount }}`

### Description

The `{{ newaccount }}` action creates a new account.

As an authorized party I {{ signer }} wish to exercise the authority of {{ creator }} to create a new account on this system named {{ name }} such that the new account's owner public key shall be {{ owner }} and the active public key shall be {{ active }}.
"
            },
            {
                "name":"onblock",
                "type":"onblock",
                "ricardian_contract":""
            },
            {
                "name":"onerror",
                "type":"onerror",
                "ricardian_contract":""
            },
            {
                "name":"refund",
                "type":"refund",
                "ricardian_contract":"# Action - `{{ refund }}`

### Description

The intent of the `{{ refund }}` action is to return previously unstaked tokens to an account after the unstaking period has elapsed. 

As an authorized party I {{ signer }} wish to have the unstaked tokens of {{ owner }} returned.
"
            },
            {
                "name":"regproducer",
                "type":"regproducer",
                "ricardian_contract":"# Action - `{{ regproducer }}`

## Description

The intent of the `{{ regproducer }}` action is to register an account as a BP candidate.

I, {{producer}}, hereby nominate myself for consideration as an elected block producer.

If {{producer}} is selected to produce blocks by the eosio contract, I will sign blocks with {{producer_key}} and I hereby attest that I will keep this key secret and secure.

If {{producer}} is unable to perform obligations under this contract I will resign my position by resubmitting this contract with the null producer key.

I acknowledge that a block is 'objectively valid' if it conforms to the deterministic blockchain rules in force at the time of its creation, and is 'objectively invalid' if it fails to conform to those rules.

{{producer}} hereby agrees to only use {{producer_key}} to sign messages under the following scenarios:
proposing an objectively valid block at the time appointed by the block scheduling algorithm
pre-confirming a block produced by another producer in the schedule when I find said block objectively valid
confirming a block for which {{producer}} has received 2/3+ pre-confirmation messages from other producers

I hereby accept liability for any and all provable damages that result from my:
signing two different block proposals with the same timestamp with {{producer_key}}
signing two different block proposals with the same block number with {{producer_key}}
signing any block proposal which builds off of an objectively invalid block
signing a pre-confirmation for an objectively invalid block
signing a confirmation for a block for which I do not possess pre-confirmation messages from 2/3+ other producers

I hereby agree that double-signing for a timestamp or block number in concert with 2 or more other producers shall automatically be deemed malicious and subject to a fine equal to the past year of compensation received and imediate disqualification from being a producer, and other damages. An exception may be made if {{producer}} can demonstrate that the double-signing occured due to a bug in the reference software; the burden of proof is on {{producer}}.

I hereby agree not to interfere with the producer election process. I agree to process all producer election transactions that occur in blocks I create, to sign all objectively valid blocks I create that contain election transactions, and to sign all pre-confirmations and confirmations necessary to facilitate transfer of control to the next set of producers as determined by the system contract.

I hereby acknowledge that 2/3+ other elected producers may vote to disqualify {{producer}} in the event {{producer}} is unable to produce blocks or is unable to be reached, according to criteria agreed to among producers.

If {{producer}} qualifies for and chooses to collect compensation due to votes received, {{producer}} will provide a public endpoint allowing at least 100 peers to maintain synchronization with the blockchain and/or submit transactions to be included. {{producer}} shall maintain at least 1 validating node with full state and signature checking and shall report any objectively invalid blocks produced by the active block producers. Reporting shall be via a method to be agreed to among producers, said method and reports to be made public.

The community agrees to allow {{producer}} to authenticate peers as necessary to prevent abuse and denial of service attacks; however, {{producer}} agrees not to discriminate against non-abusive peers.

I agree to process transactions on a FIFO best-effort basis and to honestly bill transactions for measured execution time.

I {{producer}} agree not to manipulate the contents of blocks in order to derive profit from:
the order in which transactions are included
the hash of the block that is produced

I, {{producer}}, hereby agree to disclose and attest under penalty of perjury all ultimate beneficial owners of my company who own more than 10% and all direct shareholders.

I, {{producer}}, hereby agree to cooperate with other block producers to carry out our respective and mutual obligations under this agreement, including but not limited to maintaining network stability and a valid blockchain.

I, {{producer}}, agree to maintain a website hosted at {{url}} which contains up-to-date information on all disclosures required by this contract.

I, {{producer}}, agree to set {{location}} such that {{producer}} is scheduled with minimal latency between my previous and next peer.

I, {{producer}}, agree to maintain time synchronization within 10 ms of global atomic clock time, using a method agreed to among producers.

I, {{producer}}, agree not to produce blocks before my scheduled time unless I have received all blocks produced by the prior producer.

I, {{producer}}, agree not to publish blocks with timestamps more than 500ms in the future unless the prior block is more than 75% full by either CPU or network bandwidth metrics.

I, {{producer}}, agree not to set the RAM supply to more RAM than my nodes contain and to resign if I am unable to provide the RAM approved by 2/3+ producers, as shown in the system parameters.
"
            },
            {
                "name":"regproxy",
                "type":"regproxy",
                "ricardian_contract":""
            },
            {
                "name":"rentcpu",
                "type":"rentcpu",
                "ricardian_contract":"# Action - `rentcpu`

## Description

The `rentcpu` action allows an account to rent CPU bandwidth for 30 days at a market-determined price.

As an authorized party I, {{ signer }}, wish to rent CPU bandwidth for 30 days for the use of the account {{ receiver }} in exchange for the loan payment of {{ loan_payment }}, which shall be taken from the account {{ from }}. The loan fund amount {{ loan_fund }} is set for automatic renewal of the loan at the expiry of said loan.

The amount of CPU bandwidth shall be determined by the market at time of loan execution and shall be recalculated at time of renewal, should I wish to automatically renew the loan at that time. I acknowledge that the amount of CPU bandwidth received in exchange of {{ loan_payment }} for the benefit of {{ receiver }} at loan renewal may be different from the current amount of bandwidth received. 
"
            },
            {
                "name":"rentnet",
                "type":"rentnet",
                "ricardian_contract":"# Action - `rentnet`

## Description

The `rentnet` action allows an account to rent Network bandwidth for 30 days at a market-determined price.

As an authorized party I, {{ signer }}, wish to rent Network bandwidth for 30 days for the use of the account {{ receiver }} in exchange for the loan payment of {{ loan_payment }}, which shall be taken from the account {{ from }}. The loan fund amount {{ loan_fund }} is set for automatic renewal of the loan at the expiry of said loan.

The amount of Network bandwidth shall be determined by the market at time of loan execution and shall be recalculated at time of renewal, should I wish to automatically renew the loan at that time. I acknowledge that the amount of Network bandwidth received in exchange of {{ loan_payment }} for the benefit of {{ receiver }} at loan renewal may be different from the current amount of bandwidth received. 
"
            },
            {
                "name":"rexexec",
                "type":"rexexec",
                "ricardian_contract":"# Action - `rexexec`

## Description

The `rexexec` action allows any account to perform REX maintenance by processing expired loans and unfilled sell orders.

I, {{ signer }}, wish to process up to {{ max }} of any CPU loans, Network loans, and sell orders that may currently be pending.
"
            },
            {
                "name":"rmvproducer",
                "type":"rmvproducer",
                "ricardian_contract":""
            },
            {
                "name":"sellram",
                "type":"sellram",
                "ricardian_contract":"# Action - `{{ sellram }}`

## Description

The `{{ sellram }}` action sells unused RAM for tokens.

As an authorized party I {{ signer }} wish to sell {{ bytes }} of unused RAM from account {{ account }}. 
"
            },
            {
                "name":"sellrex",
                "type":"sellrex",
                "ricardian_contract":"# Action - `sellrex`

## Description

The `sellrex` action allows an account to sell REX tokens held by the account.

As an authorized party I, {{ signer }}, wish to sell {{ rex }} REX tokens held on the account {{ from }} in exchange for core EOS tokens. If there is an insufficient amount of EOS tokens available at this time, I acknowledge that my order will be placed in a queue to be processed. 

If there is an open `sellrex` order for the account {{ from }}, then this amount of {{ rex }} REX shall be added to the existing order and the order shall move to the back of the queue. 
"
            },
            {
                "name":"setabi",
                "type":"setabi",
                "ricardian_contract":""
            },
            {
                "name":"setacctcpu",
                "type":"setacctcpu",
                "ricardian_contract":""
            },
            {
                "name":"setacctnet",
                "type":"setacctnet",
                "ricardian_contract":""
            },
            {
                "name":"setacctram",
                "type":"setacctram",
                "ricardian_contract":""
            },
            {
                "name":"setalimits",
                "type":"setalimits",
                "ricardian_contract":""
            },
            {
                "name":"setcode",
                "type":"setcode",
                "ricardian_contract":""
            },
            {
                "name":"setparams",
                "type":"setparams",
                "ricardian_contract":""
            },
            {
                "name":"setpriv",
                "type":"setpriv",
                "ricardian_contract":""
            },
            {
                "name":"setram",
                "type":"setram",
                "ricardian_contract":""
            },
            {
                "name":"setramrate",
                "type":"setramrate",
                "ricardian_contract":""
            },
            {
                "name":"setrex",
                "type":"setrex",
                "ricardian_contract":""
            },
            {
                "name":"undelegatebw",
                "type":"undelegatebw",
                "ricardian_contract":"# Action - `{{ undelegatebw }}`

## Description

The intent of the `{{ undelegatebw }}` action is to unstake tokens from CPU and/or bandwidth. 

As an authorized party I {{ signer }} wish to unstake {{ unstake_cpu_quantity }} from CPU and {{ unstake_net_quantity }} from bandwidth from the tokens owned by {{ from }} previously delegated for the use of delegatee {{ to }}. 

If I as signer am not the beneficial owner of these tokens I stipulate I have proof that Iu2019ve been authorized to take this action by their beneficial owner(s). 
"
            },
            {
                "name":"unlinkauth",
                "type":"unlinkauth",
                "ricardian_contract":""
            },
            {
                "name":"unregprod",
                "type":"unregprod",
                "ricardian_contract":"# Action - `{{ unregprod }}`

## Description

The `{{ unregprod }}` action unregisters a previously registered block producer candidate.

As an authorized party I {{ signer }} wish to unregister the block producer candidate {{ producer }}, rendering that candidate no longer able to receive votes.
"
            },
            {
                "name":"unstaketorex",
                "type":"unstaketorex",
                "ricardian_contract":"# Action - `unstaketorex`

## Description

The `unstaketorex` action allows an account to buy REX using EOS tokens which are currently staked for either CPU or Network bandwidth.

As an authorized party I, {{ signer }}, wish to buy REX tokens by unstaking {{ from_cpu }} EOS from CPU bandwidth and {{ from_net }} EOS from Network bandwidth from account {{ owner }} that are staked to account {{ receiver }}.

I am aware of, and have fulfilled, all voting requirements needed to participate in the REX marketplace.
"
            },
            {
                "name":"updateauth",
                "type":"updateauth",
                "ricardian_contract":""
            },
            {
                "name":"updaterex",
                "type":"updaterex",
                "ricardian_contract":"# Action - `updaterex`

## Description

The `updaterex` action allows an account to update its vote weight.

As an authorized party I, {{ signer }}, wish to update the REX vote stake and vote weight of the account {{ owner }}.
"
            },
            {
                "name":"updtrevision",
                "type":"updtrevision",
                "ricardian_contract":""
            },
            {
                "name":"voteproducer",
                "type":"voteproducer",
                "ricardian_contract":"# Action - `{{ voteproducer }}`

## Description

The intent of the `{{ voteproducer }}` action is to cast a valid vote for up to 30 BP candidates. 

As an authorized party I {{ signer }} wish to vote on behalf of {{ voter }} in favor of the block producer candidates {{ producers }} with a voting weight equal to all tokens currently owned by {{ voter }} and staked for CPU or bandwidth. 

If I am not the beneficial owner of these shares I stipulate I have proof that Iu2019ve been authorized to vote these shares by their beneficial owner(s). 

I stipulate I have not and will not accept anything of value in exchange for these votes, on penalty of confiscation of these tokens, and other penalties. 

I acknowledge that using any system of automatic voting, re-voting, or vote refreshing, or allowing such a system to be used on my behalf or on behalf of another, is forbidden and doing so violates this contract.
"
            },
            {
                "name":"withdraw",
                "type":"withdraw",
                "ricardian_contract":"# Action - `withdraw`

## Description

The `withdraw` action allows an account to withdraw EOS tokens from their REX fund into their liquid token balance.

As an authorized party I, {{ signer }}, wish to withdraw {{ amount }} of EOS tokens from the REX fund for the account {{ owner }} into its liquid token balance.
"
            }
        ],
        "tables":[
            {
                "name":"abihash",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"abi_hash"
            },
            {
                "name":"bidrefunds",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"bid_refund"
            },
            {
                "name":"cpuloan",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"rex_loan"
            },
            {
                "name":"delband",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"delegated_bandwidth"
            },
            {
                "name":"global",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"eosio_global_state"
            },
            {
                "name":"global2",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"eosio_global_state2"
            },
            {
                "name":"global3",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"eosio_global_state3"
            },
            {
                "name":"namebids",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"name_bid"
            },
            {
                "name":"netloan",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"rex_loan"
            },
            {
                "name":"producers",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"producer_info"
            },
            {
                "name":"producers2",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"producer_info2"
            },
            {
                "name":"rammarket",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"exchange_state"
            },
            {
                "name":"refunds",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"refund_request"
            },
            {
                "name":"rexbal",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"rex_balance"
            },
            {
                "name":"rexfund",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"rex_fund"
            },
            {
                "name":"rexpool",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"rex_pool"
            },
            {
                "name":"rexqueue",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"rex_order"
            },
            {
                "name":"userres",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"user_resources"
            },
            {
                "name":"voters",
                "index_type":"i64",
                "key_names":[

                ],
                "key_types":[

                ],
                "type":"voter_info"
            }
        ],
        "ricardian_clauses":[
            {
                "id":"EOS User Agreement",
                "body":"# EOS User Agreement

## Definitions

All capitalized, italicized, or inline code terms in *The EOS User Agreement* will be given the same effect and meaning as in *Definitions*.

* EOS User Agreement: This document (*EUA*)

* Chain ID: `chain_id` - aca376f206b8fc25a6ed44dbdc66547c36c6c33e3a119ffbeaef943642f0e906

* User: Any person or organization of persons who maintain(s) direct or indirect ownership of an EOS account, or EOS-based property connected to an EOS account.

* Ownership: Direct or indirect access to an EOS account through one or more valid permissions checks. Ownership may be partially shared between Users through the use of multi-signature permissions.

* Block Producer: Users who have called `regproducer` and receive rewards from eosio.vpay.

* `eosio.prods`: An EOS account with a dynamic permissions structure that can assume the privileges of the `eosio` account when 15/21 Block Producers agree to do so.

* Network Funds: Tokens contained within the following accounts: `eosio.names`, `eosio.ramfee`, `eosio.saving`.

* Governing Documents: *regproducer* is considered a governing document.

* On-Chain: Any transaction, smart contract, or Ricardian contract which is located within a block that is irreversible and appended to the EOS blockchain `chain_id`.

* EOS-based Property: Anything that requires a valid permission in order to directly manipulate, alter, transfer, influence, or otherwise effect on the EOS Blockchain 

* Call: To submit an action to the EOS Blockchain `chain_id`.

* Authorizations & Permissions: Permissions are arbitrary names used to define the requirements for a transaction sent on behalf of that permission. Permissions can be assigned for authority over specific contract actions.

* Ricardian Contract: A contract that places the defining elements of a legal agreement in a format that can be expressed and executed in software.

# Article I -  User Acknowledgement of Risks 
If User loses access to their EOS account on `chain_id` and has not taken appropriate measures to secure access to their EOS account by other means, the User acknowledges and agrees that that EOS account will become inaccessible. Users acknowledge that the User has an adequate understanding of the risks, usage and intricacies of cryptographic tokens and blockchain-based software. The User acknowledges and agrees that the User is using the EOS blockchain at their sole risk.

# Article II - Special User Types
Users who call `regproducer` agree to, and are bound by, the *regproducer* Ricardian Contract.

# Article III - Consent of the EUA
The nature of the *EOS User Agreement* is such that it serves as a description of the current EOS Mainnet governance functions that are in place. These functions, enforced by code, do not require the consent of Users as these functions are inherent and systemic to the EOS Mainnet itself.

# Article IV - Governing Documents
Any modifications to the *EUA* and *governing documents* may be made by `eosio.prods`. It is admonished that a statement be crafted and issued through `eosio.prods` via eosio.forum referendum contract describing such a modification in advance.

# Article V - Native Unit of Value
The native unit of value on EOS chain_id shall be the EOS token as defined and created by the `eosio.token` smart contract.

# Article VI - Maintaining the EOS blockchain
`eosio.prods` will maintain the active blockchain codebase which includes, but is not limited to, the implementation of all modifications of all features, optimizations, and upgrades: present and future. 

# Article VII - Network Funds
It is admonished that any altering of the state of any tokens contained within network fund accounts, or altering any pre-existing code that directly or indirectly governs the allocation, fulfillment, or distribution of any *network funds* be preceded by a statement crafted and issued by `eosio.prods` to the *eosio.forum* referendum system contract describing the effect in advance.

# Article VIII - Freedom of Account Creation
Any current or future User is able to create an EOS Account without the permission by any other User. `eosio.prods` may never affect an EOS User Account(s) without valid permission(s) which have been shared with `eosio.prods` by an EOS account. `eosio.prods` may charge a fee for any actions that are requested by other Users pertaining to an EOS account where permissions are shared. 

# Article IX - No Fiduciary
No User shall have a fiduciary purpose to support the value of the EOS token. No User can authorize anyone to hold assets, borrow, speak, contract on behalf of other EOS Users or the EOS blockchain `chain_id` collectively. This EOS blockchain shall have no owners, managers, or fiduciaries.

# Article X - User Security
All items pertaining to personal account security, including but not limited to the safekeeping of private keys, is solely the responsibility of the User to secure. 

# Article XI - `eosio.prods` Limited Liability
The User acknowledges and agrees that, to the fullest extent permitted by any applicable law, this disclaimer of liability applies to any and all damages or injury whatsoever caused by or related to risks of, use of, or inability to use, the EOS token or the EOS blockchain `chain_id` under any cause of action whatsoever of any kind in any jurisdiction, including, without limitation, actions for breach of warranty, breach of contract or tort (including negligence) and that `eosio.prods`, nor the individual permissions that operate it, shall not be liable for any indirect, incidental, special, exemplary or consequential damages, including for loss of profits, goodwill or data. 

### EOS 사용자 동의서 (EOS User Agreement)

#### 정의

EOS 사용자 동의서의 모든 대문자, 기울임 꼴, 또는 인라인 코드 용어는 정의에서와 동일한 효과와 의미가 부여됩니다.

- EOS 사용자 동의서: 본 문서 (EUA)
- 체인 ID: chain_id --- aca376f206b8fc25a6ed44dbdc66547c36c6c33e3a119ffbeaef943642f0e906
- 사용자: EOS 계정을 직접 또는 간접적으로 소유하거나 EOS 계정에 연결된 EOS 기반 속성을 유지하거나 관리하는 사람, 조직, 또는 조직의 모든 사람.
- 소유권: 하나 이상의 유효한 사용권한 확인을 통해 EOS 계정에 직접 또는 간접적으로 접근합니다. 소유권은 다중 서명권한을 사용하여 사용자간에 부분적으로 공유 될 수 있습니다.
- 블록 프로듀서: regproducer를 실행하고 eosio.vpay로부터 보상을 받는 사용자.
- eosio.prods: 15/21 블록 프로듀서들이 동의 할 때 eosio 계정의 권한을 가질 수 있는 동적 권한 구조를 가진 EOS 계정.
- 네트워크 자금: 다음 계정에 포함 된 토큰: eosio.names, eosio.ramfee, eosio.saving.
- 관리 문서: regproducer는 관리 문서로 간주됩니다.
- 온체인: EOS 블록체인 chain_id에 비가역적이며 추가 할 수 있는 블록 내에 위치한 모든 거래, 스마트 계약 또는 리카르디안 계약.
- EOS 기반 속성: EOS 블록체인을 직접 조작, 변경, 전송, 영향 또는 달리 적용하기 위해 유효한 사용 권한이 필요한 모든 것
- 콜: EOS 블록체인 chain_id에 작업을 신청하는 것.
- 허가 및 권한: '허가'는 해당 권한을 대신하여 전송되는 트랜잭션의 요구사항을 정의하는 데 사용됩니다. '권한'은 특정 계약 조치에 대한 권한을 부여합니다.
- 리카르디안 계약: 합법적 계약의 정의 요소를 소프트 웨어로 표현하고 실행할 수 있는 형식으로 배치하는 계약.

#### 제 1조 --- 위험에 대한 사용자들의 인지

사용자가 chain_id에서 EOS 계정에 대한 접근 권한을 잃고, 다른 방법으로 EOS 계정에 대한 접근을 보호하기 위해 적절한 조치를 취하지 않는 경우에는 EOS 계정에 접근할 수 없게 된다는 것을 인정하고 동의합니다. 사용자는 암호화 토큰과 블록체인 기반 소프트웨어의 위험, 사용법, 그리고 복잡성에 대해 충분히 이해하고 있음을 인정합니다. 사용자는 EOS 블록체인의 사용에 대한 전적인 책임을 진다는 것에 인정하고 동의합니다.

#### 제 2조 --- 특별한 사용자 유형

regproducer를 실행하는 사용자는 regproducer 리카르디안 계약에 동의하고, 이에 구속됩니다.

#### 제 3조 --- EUA의 동의

EOS 사용자 동의서는 현재 시행중인 EOS 메인넷 거 버넌스에 대한 설명으로 사용됩니다. 코드에 의해 시행되는 이러한 기능은 EOS 메인넷 자체의 체계적이고 고유한 기능이므로 사 용자의 동의를 필요로 하지 않습니다.

#### 제 4조 --- 관리 문서

EUA와 관리 문서는 eosio.prods를 통해 수정이 가능합니다. 특정 변경사항을 사전에 설명하는 eosio.forum 투표 계약을 통해 eosio.prods가 성명서를 작성하고 발급할 것을 권고합니다.

#### 제 5조 --- 가치의 기본 단위

EOS chain_id의 기본 단위는 eosio.token 스마트 계약에 의해 정의되고 작성된 EOS 토큰입니다.

#### 제 6조 --- EOS 블록체인 유지

eosio.prods는 모든 기능, 최적화, 그리고 업그레이드의 현재와 미래의 모 든 수정사항을 구현하는 것을 포함하되, 이에 국한되지 않는 활성화된 블록체인 코드베이스를 유지합니다

#### 제 7조 --- 네트워크 자금

네트워크 자금 계정에 포함된 토큰의 상태를 변경하거나, 네트워크 자금의 배분, 이행, 또는 배포를 직/간접적으로 관리하는 기존 코드를 변경하는 경우에는 eosio.prods를 eosio.forum 총 투표 시스템 계약에 추가하여 사전에 충분한 설명이 이루어져야 합니다.

#### 제 8조 --- 계정 생성의 자유

현재, 또는 미래의 사용자는 다른 사용자의 허가 없이 EOS 계정을 만들 수 있습니다. eosio.prods는 EOS 계정에 의해 공유된 유효한 허가 없이는 EOS 사용자 계정에 영향을 줄 수 없습니다. eosio.prods는 권한이 공유되는 EOS 계정과 관련하여 다른 사용자가 요청한 모든 작업에 대해 요금을 부과할 수 있습니다.

#### 제 9조 --- 신탁 불가

사용자는 EOS 토큰의 가치를 뒷받침할 수 있는 신탁 목적을 가져서는 안됩니다. 사용자는 EOS 사용자 또 는 EOS 블록체인 chain_id를 대표하여 누구에게도 자산을 보유하거나, 대여하거나, 자산에 대해 얘기하거나, 계약을 맺을 권한을 부여할 수 없습니다. EOS 블록체인에는 소유자, 관리자, 그리고 수탁자가 없어야 합니다.

#### 제 10조 --- 사용자 보안

비공개 키의 보관을 포함하되, 이에 국한되지 않는 개인 계좌 보안과 관련된 모든 항목들 또한 전적으로 사용자가 안전하게 보관해야 합니다.

#### 제 11조 --- eosio.prods 유한책임

사용자는 법률이 허용하는 한도 내에서 EOS 토큰의 위험, 사용, 또 는 사용 불가로 인해 발생하는 모든 손해에 대해 책임의 면책 조항이 적용된다는 것을 인정하고, 동의합니다. 계약 위반, 불법 행위, 그리고 위반 행위 (관리 태만 포함)와 eosio.prods 또는 이를 운영하는 개별 사용 권한을 포함하되, 이에 국한하지 않고 모든 관할 지역에서의 모든 종류의 사유로 인한 EOS 블록체인 chain_id 이익, 영업권, 또는 데이터의 손실을 포함하여 간접적, 우발적, 특수한, 대표적, 그리고 파생적인 손해에 대한 책임을 지지 않습니다.

### **定义**

EOS用户协议中的所有大写，斜体或内联代码术语将具有与以下定义相同的效果和含义。

- EOS用户协议：即本文档（EUA）

- 链上ID: chain_id - aca376f206b8fc25a6ed44dbdc66547c36c6c33e3a119ffbeaef943642f0e906

- 用户：任意满足下列要求的个人或组织：直接或者间接拥有EOS账户或与EOS账户关联的基于EOS发行的财产。

- 所有权：直接或者间接通过一个或多个有效的权限检查访问一个EOS账户。所有权可以通过 多签权限许可在用户间共享。

- 执行了regproduce，并且从eosio.vpay领取收入的用户。

- eosio.prods:具有动态权限结构的EOS帐户，当15/21 Block Producers同意时，该帐户可以承担eosio帐户的权限。

- 网络资产：包含在以下账户中的代币：eosio.names、eosio.ramfee、 eosio.saving。

- 治理文档：regproducer是治理文档。

- 任何交易、智能合约或者李嘉图合约，它们已经 位于一个区块中，并且这个区块是不可逆转的、已附加到名为chain_id的EOS区块链中。

- 基于EOS资产：任何需要有效许可来操作、改变、转移、影响或者进行其他操作的东西。

- 执行：在名为chain_id的EOS区块链中提交一个行动。

- 授权和权限：权限（Permissions）是用来定义代表该权限发送的交易的要求的任意名字。可以给特定的合约操作的授权（Authorizations）分配权限（Permissions）。

- 李嘉图合约：将法律协议中的定义要素以能在软件中表达和执行的格式表达的合约。

### **条款一****用****户风险 确认**

如果用户丢失账户访问权限或者没有采取合适的方式保护账户访问权限，用户应知悉并同意，EOS账户将无法访问。用户应确 认用户对加密代币和区块链软件的风险、用法和复杂性有充分了解。用户承认并同意用户自行承担使用EOS区块链的风险。

### **条 款二****特殊用****户类型**

执行regproduce，同意并且受regproducer李嘉图合约约束的用户。

### **条款三****同意****EOS****用****户协议**

EOS用户协议的实质是对当前EOS主网治理功能的描述。由代码强制执行的功能不需要用户的同意，因为这些功能是EOS主网系统自带的。

### **条款四** - **治理文档**

eosio.prods可以对EOS用户协议和治理文档进行任何修改。严正提醒，提前用eosio.forum公投合约，通过eosio.prods编写、发布一个声明来描述那个修改。

### **条款五****原生价****值单位**

EOS公链上的原生价值单位应为eosio.token智能合约定义和创建的EOS通证。

### **条款六****维护****EOS****区****块链**

无论现在或将来将来，eosio.prods将维护活跃的区块链代码库，包括但不限于所有功能、优化、升级的所有修改、实现。

### 条款七 - ****定****义****EOS****网络资产

更改网络资产账户中的任何代币的状态，更改任何现存的直接或间接管理任何网络资产的分配、 实现或分发的代码，需要事先用eosio.prods在eosio.forum公投合约上编写和发布效果描述的声明。

### **条款八-创建账户自由**

任何现在或将来的用户都可以在未经任何其他用户许可的情况下创建EOS帐户。 如何没有收到EOS帐户的有效许可（permission），eosio.prods永远不会影响EOS用户帐户。 对于共享权限的EOS帐户的其他用户请求的任何操作，eosio.prods可能会收取费用。

### **条款九没有受托人**

没有用户承担信托责任来维持EOS代币的价值。没有用户可以代表EOS用户或者代表名为chain_ID的EOS区块链授权任何人共同持有资产、借款、发言或定合同。此区块链不存在拥有者、管理者或者受托人。

### **条款十个人安全**

所有有关个人账户安全的事项，包括但不限于私钥的安全保存，都由用户自己负责。

### **条款十一 eosio.prods的有限责任**

用户应知悉和同意，在任何适用法律允许的最大范围内，本免责声明适用于与EOS代币风险，使用或无法使用EOS代币有关或导致的任何或所有损害或伤害，也适用于任何司法管辖区内的任何任何行为下的EOS区块链chain_id，包括但不限于违反担保、违反合同或侵权行为（包括疏忽 ）。eosio.prods以及操作它的个人权限对于任何间接的，偶然的，特殊的，示例性的或后果性的损害，包括利润损失，商誉或数据，不 承担任何责任。"
            }
        ],
        "error_messages":[

        ],
        "abi_extensions":[

        ],
        "variants":[

        ]
    }
}
```