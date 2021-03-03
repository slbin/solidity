# solidity
Solidity Study

# References
https://docs.soliditylang.org/
https://ethereum.org/en/
https://confluxnetwork.org/
https://www.youtube.com/watch?v=_V7MntH_Tu8
https://www.youtube.com/watch?v=ipwxYa-F1uY

## what is ethereum?
Ethereum is open access to digital money and data-friendly services for everyone – no matter your background or location. It's a community-built technology behind the cryptocurrency ether (ETH) and thousands of applications you can use today.

## What is ETH?
ETH is a cryptocurrency. It is scarce digital money that you can use on the internet – similar to Bitcoin. If you’re new to crypto, here's how ETH is different from traditional money.


## Env
https://nodejs.org/en/download/
https://github.com/coreybutler/nvm-windows#node-version-manager-nvm-for-windows



## QinYuan
https://github.com/Fabsqrt/
https://www.youtube.com/watch?v=_V7MntH_Tu8

GFS --> Hadoop
P2P maze lobster emule

Blockchain --> Distributed Database  --> link of list

How to store data incrementally
How to modify data
Modify and Store separately

```
class DataBlock{
    getData();
    setData();
    getPre();
    getNext();
}
```
Unmodifiable linked datablock

Bitcoin supports programing but not good
Ethereum good


data state compute
storage transaction contract

N Copy -- Full Copy
Read/Write ?

## Nativecoin


## Block
index
timestamp
data
Hash: SHA256
previous Hash

``` ts
class Block 
    public index: number;
    public hash: string;
    public previousHash: string
    public timestamp: number
    public data: string
    
    constructor(indx: number, hash: string, previousHash, string, timestamp: number, data: string): string =>
        CryptoJS.SHA256(index + previousHash + timestamp + data).toString();
```

The first block?
```ts
const genesisBlock: Block = new Block(0, 'XXX', null, 142495938, 'my genesis block')
```
How to create new block
```ts
const genereateNextBlock = (blockData: string) =>
{
    const previousBlock: Block = getLatestBlock();
    const nextIndex: number = previousBlock.index + 1;
    ...
}；
```
where to store block
const blockchain: Block[] = [genesisBlock]


How to validate blockdata
- +1
- previousHash
- Hash
- type of data

How to valiadate blockchain data

chain bifurcate

Sync between two nodes
Gossip agreement broadcast

system architect
blockchain --websocket interface  for P2P communication with other nodes
|                                    
https interface
for controlling the node


Hyper attack

Computation power: an open fair axam: POW proof of work 
Problem:  to find a block, the Hash of this block has a special prefix

Nonce
++n >> n++

How to define the difficulty
- Block generation interval : BTC 10 min, ETH 10-20s
- Difficulty adjustment interval



中本聪共识

长度 X 计算复杂度 O

 


