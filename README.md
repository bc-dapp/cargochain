# Cargochain Installation

Follow the [Official Repo to install](https://github.com/domschiener/cargochain), or just follow along.

# Dependencies and Prerequisites

Have a working install of the following
- Ethereum
- IPFS
- Meteor JS
- Metamask Chrome Extension (optional, recommended)

## Set up Ethereum Network

### Private Network

#### Custom Genesis Setup

Create a new folder and input the following genesis code into a json file

    $ mkdir -p eth-private-net
    $ vim custom_genesis.json // Or whatever code editor you may use

Inside...

	{
		"config": {
			"chainId" : 8520,
			"homesteadBlock" : 10
		},
		"nonce": "0x0000000000000042", 
		"mixhash": "0x0000000000000000000000000000000000000000000000000000000000000000", 
		"difficulty": "0x00400", 
		"coinbase": "0x3333333333333333333333333333333333333333", 
		"timestamp": "0x0", 
		"parentHash": "0x0000000000000000000000000000000000000000000000000000000000000000", 
		"extraData": "", 
		"gasLimit": "0x800000000",
		"alloc": {}
	}

Change anything within those block. You're a free (wo)man

Run the following to initialize
    
    $ geth init custom_genesis.json --datadir data

which will create a `data` folder and initialize geth
    
#### Running

    $ geth --nodiscover --datadir data console // Add --networkid=100 if it doesn't work

It should all be set up.

### Public Net

**WIP**

## IPFS

Check online for installation

## Meteor

Check online for installation

## Metamask

Check online for installation

# Running

Make sure ethereum and ipfs daemon are running. 

Clone cargochain, and `cd` to `cargochain/app` and run

    $ meteor

_To be continued_

# TODO

- [ ] Link Metamask + cargochain
- [ ] Finish this documentation
