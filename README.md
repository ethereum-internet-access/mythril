# mythril
Usage of Mythril security analysis tool

Mythril is a security analysis tool for EVM bytecode. It detects security vulnerabilities in smart contracts built for Ethereum. We will analyze the Solidity-based smart contract called StateChannel.sol (of this project).

## How to use it

### Update
$ sudo apt update

### Install solc
$ sudo apt install software-properties-common  
$ sudo add-apt-repository ppa:ethereum/ethereum  
$ sudo apt install solc  

### Install libssl-dev, python3-dev, and python3-pip
$ sudo apt install libssl-dev python3-dev python3-pip

### Install mythril
$ pip3 install mythril

### You might need to install a dependency (python-dateutil==2.8.0)
$ pip3 install python-dateutil==2.8.0

### Option A) Analyze local source code
$ cd contracts  
$ myth analyze StateChannel.sol > ./security-report  
$ cat ./security-report  

### Option B) Analyze on-chain smart contract (e.g., on Ropsten)
$ myth analyze --rpc infura-ropsten -a contract-address > ./security-report  
$ cat ./security-report  
