





Instructions on how to use the chain for the rest of your team.

- We need to start the node from the directory where we created the Blockchain. See screenshot below.
- instructions to start up the 2 nodes.



```
MINER OPTIONS:
  --mine                              Enable mining
```

```
NETWORKING OPTIONS:
  --bootnodes value                   Comma separated enode URLs for P2P discovery bootstrap
```

### Bootnode

[Bootnode](https://github.com/ethereum/go-ethereum/wiki/Setting-up-private-network-or-local-cluster#setup-bootnode) is a lightweight application used for the [Node Discovery Protocol](https://github.com/ethereum/devp2p/blob/master/rlpx.md#node-discovery). Bootnodes do not sync chain data. Using a UDP-based [Kademlia](https://en.wikipedia.org/wiki/Kademlia)-like RPC protocol, Ethereum will connect and interrogate these bootnodes for the location of potential peers. The Ethereum Foundation maintains several bootnodes for the public Ethereum networks; the endpoints of which are [hard-coded in the Geth source code](https://github.com/ethereum/go-ethereum/blob/master/params/bootnodes.go). The default list can be configured using the `--bootnodes` option:

```
geth --bootnodes [enode://pubkey1@ip1:port1,enode://pubkey2@ip2:port2,…]
```



```
API AND CONSOLE OPTIONS:
  --ipcdisable                        Disable the IPC-RPC server
```



```
ACCOUNT OPTIONS:
```

```
 --allow-insecure-unlock             Allow insecure account unlocking when account-related RPCs are exposed by http
```



The ethereum CLI `geth` provides account management via the `account` command:

```
$ geth account <command> [options...] [arguments...]
```

Manage accounts lets you create new accounts, list all existing accounts, import a private key into a new account, migrate to newest key format and change your password.

Keys are stored under `<DATADIR>/keystore`. 

When you install Geth with helper tools, it comes with a handy tool called Puppeth, which you can use to maintain and install various helper tools for managing and deploying your private blockchain.

Reference - https://geth.ethereum.org/docs/interface/managing-your-accounts





# Puppeth network manager

Do you *like* setting up a private network? Don’t answer that! Truth be told, if you’ve ever tried to set up your own private Ethereum network - whether for friendly fun, corporate work, or hackathon aid - you’ll certainly know the pain it takes to do so. Configuring a genesis block is one thing, but when you get to bootnodes, full nodes, miners and light clients, things start to wear thin fast… and we haven’t even talked about monitoring, explorers, faucets, wallets. It’s a mess.

Geth 1.6 ships a new tool called `puppeth`, which aims to solve this particular pain point. Puppeth is a CLI wizard that aids in creating a new Ethereum network down to the genesis, bootnodes, signers, ethstats, faucet, dashboard and more, without the hassle that it would normally take to configure all these services one by one. Puppeth uses ssh to dial into remote servers, and builds its network components out of docker containers using docker-compose. The user is guided through the process via a command line wizard that does the heavy lifting and topology configuration automatically behind the scenes.

Puppeth is not a magic bullet. If you have large in-house Ethereum deployments based on your own orchestration tools, it’s always better to use existing infrastructure. However, if you need to create your own Ethereum network without the fuss, Puppeth might actually help you do that… fast. Everything is deployed into containers, so it will not litter your system with weird packages. That said, it’s Puppeth’s first release, so tread with caution and try not to deploy onto critical systems.

Reference - https://blog.ethereum.org/2017/04/14/geth-1-6-puppeth-master/



![image-20210820110301824](C:\Users\chakravartiraghavan\AppData\Roaming\Typora\typora-user-images\image-20210820110301824.png)





Starting Node 1 - 

![image-20210820111327169](C:\Users\chakravartiraghavan\AppData\Roaming\Typora\typora-user-images\image-20210820111327169.png)





Starting Node 2 - 

![image-20210820111240138](C:\Users\chakravartiraghavan\AppData\Roaming\Typora\typora-user-images\image-20210820111240138.png)











New wallet created - had balance 0.



![image-20210820110144424](C:\Users\chakravartiraghavan\AppData\Roaming\Typora\typora-user-images\image-20210820110144424.png)





Node 1 wallet below: 

![image-20210820110357219](C:\Users\chakravartiraghavan\AppData\Roaming\Typora\typora-user-images\image-20210820110357219.png)





Now send 1 ETH from Node 1 to New wallet created.

![image-20210820110540705](C:\Users\chakravartiraghavan\AppData\Roaming\Typora\typora-user-images\image-20210820110540705.png)







![image-20210820110719876](C:\Users\chakravartiraghavan\AppData\Roaming\Typora\typora-user-images\image-20210820110719876.png)









![image-20210820110731706](C:\Users\chakravartiraghavan\AppData\Roaming\Typora\typora-user-images\image-20210820110731706.png)





![image-20210820110805294](C:\Users\chakravartiraghavan\AppData\Roaming\Typora\typora-user-images\image-20210820110805294.png)







Now New wallet has the 1 ETH balance.

![image-20210820110935755](C:\Users\chakravartiraghavan\AppData\Roaming\Typora\typora-user-images\image-20210820110935755.png)















