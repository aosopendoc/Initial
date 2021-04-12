# Initial

## One. AOS base info, you can know AOS from EOS,because they use almost same technology
### 1.EOS souce code
https://github.com/EOSIO/eos
### 2.EOS Contract compile environment
https://github.com/EOSIO/eosio.cdt
### 3.EOS Core contract
https://github.com/EOSIO/eosio.contracts


## Two. EOS http rpc api docment
http://cw.hubwiz.com/card/c/eos-rpc-api/

## Three. claos is same with cleos,the cleos command document
http://cw.hubwiz.com/card/c/cleos/1/1/1/


## Four. AOS develop by java
### 1.a project with java14 and sprint boot(includes transfer and create account example)you can open by Intelij Idea 2020.3
https://github.com:aosopendoc/AosServerByJava.git


### 2.a project running on Android example(includes almost all use case:transfer,create account,get balance,gennerate privateKey)
https://github.com/swapnibble/EosCommander



## Five. How to charge at ‘Centralized exchange’
eg. user A want to charge '100.0000 AOS' to account 'centralizede' proviede by ‘Centralized exchange’
### 1. gen a unique id(for exmaple 1234) for user A, must unique for every user
### 2. user A transfer '100.0000 AOS' to account 'centralizede', must with memo '1234'
### 3. ‘Centralized exchange’ get_actions to detech weather has new transfer（distinguish the transfer is from who by memo）,and deal this transfer,and then charge to the ‘Centralized exchange’ for this user A
```
curl -X POST --url http://127.0.0.1:8888/v1/history/get_actions -d '{
  "pos": -1,
  "offset": -20,
  "account_name": "centralizede"
}'
```