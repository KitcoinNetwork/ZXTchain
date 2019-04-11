# ZXT chain

## Install

* Currently install an POA ethereum instance:
	* install geth 1.8 or 1.9
	* initialize server private keys
	* copy `zxt.json` in local directory
	* initialize chain with 'geth --datadir serverdir/ init zxt.conf'
	* start with `/home/zxt/go-ethereum/build/bin/geth --datadir testnode --syncmode 'fast' --port 30382 --networkid 66448668 -unlock '0xf5911028a116e30b06c57f44505b76e7e3906741' --password testnode/password.txt --ethstats ZXT_testnode:ask_password@47.244.51.138`
	* ethstats password: ask dev@kitcoin.info
	* current node list: ask dev@kitcoin.info
