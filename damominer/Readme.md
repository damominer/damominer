# DamoMiner

GPU miner for ETH,CKB,ETH-CKB

# Help

GPU miner,it is only support Nvidia card now !

 Options :

    -P,--pool           Stratum pool. Example
                        ckb pool: stratum+tcp://youraccount.workname@ckb-eu.sparkpool.com:8888
                        eth pool: stratum1+tcp://youraccount.workname@cn.sparkpool.com:3333
                        scheme://[account[.workername]@]hostname:port

    -E                  Dual ming mode, set ETH pool, single ming mode only need set -P 
                        scheme://[account[.workername]@]hostname:port

    -A                  Algorithm supported:ckb,eth,eth_ckb
    -h,--help           Displays this help text and exits
    -V,--version        Show program version and exits
    --api-bind          Default not set. Example:--api-bind 127.0.0.1:3333
                        Use negative port number for readonly mode
    --api-port          Default not set.range from (1~65535) 
                        listen on this port 
    --api-password      Default not set.you can set the password to protect your interaction


# Requirements

##  Linux 

    NVIDIA Driver version:>=418,cuda 10.1

## window 

    support cuda9、cuda10

# Performance




# Sample Usages

## ETH

### Linux

    damominer -P stratum1+tcp://youraccount.workname@cn.sparkpool.com:3333 -A eth  --api-bind 127.0.0.1:3333

### Window

    damominer.exe -P stratum1+tcp://youraccount.workname@cn.sparkpool.com:3333 -A eth 

## CKB

### Linux

    damominer -P stratum+tcp://youraccount.workname@ckb.sparkpool.com:8888 -A ckb

### Window

    damominer.exe -P stratum+tcp://youraccount.workname@ckb.sparkpool.com:8888  -A ckb 

## ETH-CKB

### Linux

    damominer -P stratum1+tcp://youraccount.workname@cn.sparkpool.com:3333 -E stratum1+tcp://youraccount.workname@cn.sparkpool.com:3333 -A eth_ckb

### Window

    damominer.exe -P stratum+tcp://youraccount.workname@ckb.sparkpool.com:8888  -E stratum1+tcp://youraccount.workname@cn.sparkpool.com:3333 -A eth_ckb --mode 1

# API Reference

    {
    "id": 1,
    "jsonrpc": "2.0",
    "method": "miner_getstatdetail"
    }

    response:
    {
        "id": 0,
        "jsonrpc": "2.0",
        "result": {
            "connection": {
                "connected": true,
                "switches": 1,
                "uri": "stratum+tcp://youraccount.workname@ckb.sparkpool.com:8888"
            },
            "devices": [
                {
                    "_index": 0,
                    "_mode": "CUDA",
                    "hardware": {
                        "name": "P102-100 9.92 GB",
                        "pci": "06:00.0",
                        "sensors": [
                            0,
                            0,
                            0
                        ],
                        "type": "GPU"
                    },
                    "mining": {
                        "hashrate": "0x000847f9",
                        "hashrate_sc": "0x22074180",
                        "segment": [
                            "0xe9624dbb2939f091",
                            "0xe9624dbc2939f091"
                        ],
                        "shares": [
                            0,//accept share;
                            0,//reject share;
                            0,//fault share;
                            18   //last share take delay_time;
                        ]
                    }
                },
                {
                    "_index": 1,
                    "_mode": "CUDA",
                    "hardware": {
                        "name": "P102-100 9.92 GB",
                        "pci": "07:00.0",
                        "sensors": [
                            0,
                            0,
                            0
                        ],
                        "type": "GPU"
                    },
                    "mining": {
                        "hashrate": "0x00085c1c",
                        "hashrate_sc": "0x211add80",
                        "segment": [
                            "0xe9624dbc2939f091",
                            "0xe9624dbd2939f091"
                        ],
                        "shares": [
                            0,
                            0,
                            0,
                            18
                        ]
                    }
                },
                {
                    "_index": 2,
                    "_mode": "CUDA",
                    "hardware": {
                        "name": "P102-100 9.92 GB",
                        "pci": "0a:00.0",
                        "sensors": [
                            0,
                            0,
                            0
                        ],
                        "type": "GPU"
                    },
                    "mining": {
                        "hashrate": "0x00084db2",
                        "hashrate_sc": "0x216dbc00",
                        "segment": [
                            "0xe9624dbd2939f091",
                            "0xe9624dbe2939f091"
                        ],
                        "shares": [
                            0,
                            0,
                            0,
                            18
                        ]
                    }
                },
                {
                    "_index": 3,
                    "_mode": "CUDA",
                    "hardware": {
                        "name": "P102-100 9.92 GB",
                        "pci": "0b:00.0",
                        "sensors": [
                            0,
                            0,
                            0
                        ],
                        "type": "GPU"
                    },
                    "mining": {
                        "hashrate": "0x0008400d",
                        "hashrate_sc": "0x1e64aec0",
                        "segment": [
                            "0xe9624dbe2939f091",
                            "0xe9624dbf2939f091"
                        ],
                        "shares": [
                            0,
                            0,
                            0,
                            18
                        ]
                    }
                },
                {
                    "_index": 4,
                    "_mode": "CUDA",
                    "hardware": {
                        "name": "P102-100 9.92 GB",
                        "pci": "0c:00.0",
                        "sensors": [
                            0,
                            0,
                            0
                        ],
                        "type": "GPU"
                    },
                    "mining": {
                        "hashrate": "0x00085f42",
                        "hashrate_sc": "0x1d059480",
                        "segment": [
                            "0xe9624dbf2939f091",
                            "0xe9624dc02939f091"
                        ],
                        "shares": [
                            0,
                            0,
                            0,
                            18
                        ]
                    }
                }
            ],
            "host": {
                "name": "N0101",
                "runtime": 18,
                "version": "damominer"
            },
            "mining": {
                "difficulty": 99998604623,
                "epoch": -1,
                "epoch_changes": 0,
                "hashrate": "0x00299118",
                "shares": [//master coin
                    0,//accept share;
                    0,//reject share;
                    0,//fault share;
                    18   //last share take delay_time;
                ]
                "shares_sc": [//slave coin
                    0,//accept share;
                    0,//reject share;
                    0,//fault share;
                    18   //last share take delay_time;
                ]
            },
            "monitors": null
        }
    }

# History

## V2.4.3 (20200207)

    support ETH,CKB,ETH-CKB Dual ming.
    support Window & linux.
