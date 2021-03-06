# ZXT chain

## Install

Currently install an POA ethereum instance:

- install geth 1.8 or 1.9
	* `git clone https://github.com/ethereum/go-ethereum`
	* `cd go-ethereum`
	* `make geth`
	* `ln -s build/bin/geth /usr/bin/geth`
- initialize server private keys
	* `cd /data/`
	* `mkdir MYNODE`
	* `geth --datadir MYNODE/ account new`
	* write password in `MYNODE/password.txt`
	* key should be created in `MYNODE/keystore/`, use PUBKEY when starting geth instance
- copy `zxt.json` in local directory
	* `wget https://raw.githubusercontent.com/KitcoinNetwork/ZXTchain/master/zxt.json`
- initialize chain:
	* `geth --datadir MYNODE/ init zxt.json`
	* initial block hash should be 0xb14a673aac716d9c8834a7194295b18a8a397e94124d089c9fa1c70022279db6
- start instance:
	* `/home/zxt/go-ethereum/build/bin/geth --datadir MYNODE --syncmode 'fast' --port 30382 --networkid 66448668 -unlock 'PUBKEY' --password MYNODE/password.txt --ethstats ZXT_testnode:ask_password@47.244.51.138`
- ethstats password: ask dev@kitcoin.info
- current node list: ask dev@kitcoin.info
	* write enode list in `mynode/static-nodes.json`
	* OR: in geth console (`geth attach MYNODE/geth.ipc`), `admin.addPeer("enode://balabalaHASH@155.155.155.155:1234")`
	* test: in geth console type: `admin.peers`  and check that there are peers