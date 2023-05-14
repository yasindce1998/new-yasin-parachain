# Polkadot Substrate Cumulus Parachain

This project introduces a new Substrate node based on Cumulus. It provides a simplified implementation of a parachain using the Substrate framework within the Polkadot ecosystem.

## Overview
This project aims to demonstrate the integration of Substrate Cumulus parachain into a blockchain network. The Substrate Cumulus parachain provides a framework for building and deploying custom blockchains, allowing developers to create their own specialized chains while leveraging the security and scalability of the Polkadot ecosystem.

**Features**

- **Custom Blockchain Development:** The project showcases the development of a custom blockchain using Substrate Cumulus parachain. This allows developers to define and implement their own blockchain logic, consensus mechanisms, and economic models tailored to specific use cases.

- **Polkadot Interoperability:** By integrating the Substrate Cumulus parachain, the custom blockchain becomes interoperable with the wider Polkadot network. This enables seamless communication and data transfer between parachains, allowing for enhanced scalability and cross-chain functionalities.

- **Security and Scalability:** Leveraging the security guarantees and scalability features of the Polkadot ecosystem, the project ensures that the custom blockchain built on Substrate Cumulus parachain inherits the robustness and performance of the underlying network.

- **Consensus Mechanism Configuration:** The project provides examples and guidelines for configuring consensus mechanisms within the Substrate Cumulus parachain. Developers can choose from various consensus algorithms, such as Proof of Stake (PoS) or Practical Byzantine Fault Tolerance (PBFT), based on the specific requirements of their custom blockchain.

- **Governance and Upgradability:** The Substrate Cumulus parachain integration demonstrates the implementation of on-chain governance mechanisms, allowing stakeholders to participate in decision-making processes and propose upgrades to the blockchain. This ensures long-term sustainability and adaptability of the custom blockchain.

## System Requirements
Verify your system requirement using `substrate-benchmark-machine` tool.


## To Build a parahain
- Download [polkadot](https://github.com/paritytech/polkadot/releases/download/v0.9.42/polkadot) binary.
- Open your terminal and execute this command.
- To create chain specification refer [this](https://docs.substrate.io/build/chain-spec/) document.
```sh
➜  Downloads ./polkadot \
--alice \
--validator \
--base-path /tmp/relay/alice \
--chain /tmp/raw-local-chainspec.json \
--port 30333 \
--ws-port 9944 \
--bootnodes /ip4/127.0.0.1/tcp/30333/p2p/12D3KooWEzJVmzxpPDGAExpSqFgWHjxeqs6vZ4NEQHKCaSDkMwb5
```

- Open another terminal execute this command
```sh
➜  Downloads ./polkadot \  
--bob \
--validator \
--base-path /tmp/relay-bob \
--chain /tmp/raw-local-chainspec.json \
--port 30334 \
--ws-port 9945
```

- Now you have two nodes with relaychain. \
(For the bootnode make sure to check for this and put appropriate values `🏷  Local node identity is: 12D3KooWEzJVmzxpPDGAExpSqFgWHjxeqs6vZ4NEQHKCaSDkMwb5`)

- To create a local parachain do the below commands.
```sh
git clone https://github.com/yasindce1998/new-yasin-parachain.git
cd new-yasin-parachain
cargo build --release
```
_Note: This will take some time to build and after finish building the project._

```sh
./target/release/parachain-template-node --help
```
_Note: Run this command to make sure if your build is built correctly._

- To connect to a local parachain refer [this](https://docs.substrate.io/tutorials/build-a-parachain/connect-a-local-parachain/) document.

- After that execute the build binary like shown below.
```shell
./target/release/parachain-template-node \
--alice \
--collator \
--force-authoring \
--chain raw-parachain-chainspec.json \
--base-path /tmp/parachain/alice \
--port 40333 \
--ws-port 8844 \
-- \
--execution wasm \
--chain /tmp/raw-local-chainspec.json \
--port 30343 \
--ws-port 9977 \
--bootnodes /ip4/127.0.0.1/tcp/40333/p2p/12D3KooWDUX4kvd9mYvhgBaQsSq2Mq6Y5yKfrVPSvEC31N2oYoEm
```

<details>
  <summary>Output</summary>

```sh
➜  new-yasin-parachain git:(main) ✗ ./target/release/parachain-template-node \
--alice \
--collator \
--force-authoring \
--chain raw-parachain-chainspec.json \
--base-path /tmp/parachain/alice \
--port 40333 \
--ws-port 8844 \
-- \
--execution wasm \
--chain /tmp/raw-local-chainspec.json \
--port 30343 \
--ws-port 9977 \
--bootnodes /ip4/127.0.0.1/tcp/40333/p2p/12D3KooWDUX4kvd9mYvhgBaQsSq2Mq6Y5yKfrVPSvEC31N2oYoEm
2023-05-13 23:39:51 Parachain Collator Template    
2023-05-13 23:39:51 ✌️  version 0.1.0-e6ee3ba4746    
2023-05-13 23:39:51 ❤️  by Anonymous, 2020-2023    
2023-05-13 23:39:51 📋 Chain specification: Local Testnet    
2023-05-13 23:39:51 🏷  Node name: Alice    
2023-05-13 23:39:51 👤 Role: AUTHORITY    
2023-05-13 23:39:51 💾 Database: RocksDb at /tmp/parachain/alice/chains/local_testnet/db/full    
2023-05-13 23:39:51 ⛓  Native runtime: template-parachain-1 (template-parachain-0.tx1.au1)    
2023-05-13 23:39:55 Parachain id: Id(2000)    
2023-05-13 23:39:55 Parachain Account: 5Ec4AhPUwPeyTFyuhGuBbD224mY85LKLMSqSSo33JYWCazU4    
2023-05-13 23:39:55 Parachain genesis state: 0x000000000000000000000000000000000000000000000000000000000000000000f6d5d785fc1792fae673be2c50bd91b133d6e66778b3b9483fdbe62ceb9391aa03170a2e7597b7b7e3d84c05391d139a62b157e78786d8c082f29dcf4c11131400    
2023-05-13 23:39:55 Is collating: yes    
2023-05-13 23:40:03 [Relaychain] 👶 Creating empty BABE epoch changes on what appears to be first startup.    
2023-05-13 23:40:03 [Relaychain] 🏷  Local node identity is: 12D3KooWDUX4kvd9mYvhgBaQsSq2Mq6Y5yKfrVPSvEC31N2oYoEm    
2023-05-13 23:40:03 [Relaychain] 💻 Operating system: linux    
2023-05-13 23:40:03 [Relaychain] 💻 CPU architecture: x86_64    
2023-05-13 23:40:03 [Relaychain] 💻 Target environment: gnu    
2023-05-13 23:40:03 [Relaychain] 💻 CPU: Intel(R) Core(TM) i5-5300U CPU @ 2.30GHz    
2023-05-13 23:40:03 [Relaychain] 💻 CPU cores: 2    
2023-05-13 23:40:03 [Relaychain] 💻 Memory: 7837MB    
2023-05-13 23:40:03 [Relaychain] 💻 Kernel: 5.19.0-38-generic    
2023-05-13 23:40:03 [Relaychain] 💻 Linux distribution: Ubuntu 22.04.2 LTS    
2023-05-13 23:40:03 [Relaychain] 💻 Virtual machine: no    
2023-05-13 23:40:03 [Relaychain] 📦 Highest known block at #0    
2023-05-13 23:40:03 [Relaychain] 〽️ Prometheus exporter started at 127.0.0.1:9616    
2023-05-13 23:40:03 [Relaychain] Running JSON-RPC HTTP server: addr=127.0.0.1:9934, allowed origins=["http://localhost:*", "http://127.0.0.1:*", "https://localhost:*", "https://127.0.0.1:*", "https://polkadot.js.org"]    
2023-05-13 23:40:03 [Relaychain] Running JSON-RPC WS server: addr=127.0.0.1:9977, allowed origins=["http://localhost:*", "http://127.0.0.1:*", "https://localhost:*", "https://127.0.0.1:*", "https://polkadot.js.org"]    
2023-05-13 23:40:03 [Relaychain] 🏁 CPU score: 930.89 MiBs    
2023-05-13 23:40:03 [Relaychain] 🏁 Memory score: 7.32 GiBs    
2023-05-13 23:40:03 [Relaychain] 🏁 Disk score (seq. writes): 102.98 MiBs    
2023-05-13 23:40:03 [Relaychain] 🏁 Disk score (rand. writes): 27.76 MiBs    
2023-05-13 23:40:03 [Relaychain] Starting with an empty approval vote DB.
2023-05-13 23:40:03 [Parachain] 🏷  Local node identity is: 12D3KooWMzPXFQ2bNRFsbK78mNE7LKZTFGm15qsKqkKLU8MaVneq    
2023-05-13 23:40:03 [Parachain] 💻 Operating system: linux    
2023-05-13 23:40:03 [Parachain] 💻 CPU architecture: x86_64    
2023-05-13 23:40:03 [Parachain] 💻 Target environment: gnu    
2023-05-13 23:40:03 [Parachain] 💻 CPU: Intel(R) Core(TM) i5-5300U CPU @ 2.30GHz    
2023-05-13 23:40:03 [Parachain] 💻 CPU cores: 2    
2023-05-13 23:40:03 [Parachain] 💻 Memory: 7837MB    
2023-05-13 23:40:03 [Parachain] 💻 Kernel: 5.19.0-38-generic    
2023-05-13 23:40:03 [Parachain] 💻 Linux distribution: Ubuntu 22.04.2 LTS    
2023-05-13 23:40:03 [Parachain] 💻 Virtual machine: no    
2023-05-13 23:40:03 [Parachain] 📦 Highest known block at #0    
2023-05-13 23:40:03 [Parachain] Running JSON-RPC HTTP server: addr=127.0.0.1:42285, allowed origins=["http://localhost:*", "http://127.0.0.1:*", "https://localhost:*", "https://127.0.0.1:*", "https://polkadot.js.org"]    
2023-05-13 23:40:03 [Parachain] Running JSON-RPC WS server: addr=127.0.0.1:8844, allowed origins=["http://localhost:*", "http://127.0.0.1:*", "https://localhost:*", "https://127.0.0.1:*", "https://polkadot.js.org"]    
2023-05-13 23:40:03 [Parachain] 🏁 CPU score: 930.89 MiBs    
2023-05-13 23:40:03 [Parachain] 🏁 Memory score: 7.32 GiBs    
2023-05-13 23:40:03 [Parachain] 🏁 Disk score (seq. writes): 102.98 MiBs    
2023-05-13 23:40:03 [Parachain] 🏁 Disk score (rand. writes): 27.76 MiBs    
2023-05-13 23:40:03 [Parachain] ⚠️  The hardware does not meet the minimal requirements for role 'Authority'.    
2023-05-13 23:40:08 [Relaychain] 💤 Idle (0 peers), best: #0 (0xcb14…d6d8), finalized #0 (0xcb14…d6d8), ⬇ 0 ⬆ 0    
2023-05-13 23:40:08 [Parachain] 💤 Idle (0 peers), best: #0 (0x3f02…95ab), finalized #0 (0x3f02…95ab), ⬇ 1.6kiB/s ⬆ 1.3kiB/s    
2023-05-13 23:40:13 [Relaychain] discovered: 12D3KooWMzPXFQ2bNRFsbK78mNE7LKZTFGm15qsKqkKLU8MaVneq /ip4/192.168.76.77/tcp/40333    
2023-05-13 23:40:13 [Relaychain] discovered: 12D3KooWMzPXFQ2bNRFsbK78mNE7LKZTFGm15qsKqkKLU8MaVneq /ip4/192.168.49.1/tcp/40333    
2023-05-13 23:40:13 [Relaychain] discovered: 12D3KooWMzPXFQ2bNRFsbK78mNE7LKZTFGm15qsKqkKLU8MaVneq /ip4/10.42.0.1/tcp/40333    
2023-05-13 23:40:13 [Relaychain] 💤 Idle (0 peers), best: #0 (0xcb14…d6d8), finalized #0 (0xcb14…d6d8), ⬇ 0 ⬆ 0    
2023-05-13 23:40:13 [Parachain] 💤 Idle (0 peers), best: #0 (0x3f02…95ab), finalized #0 (0x3f02…95ab), ⬇ 0.3kiB/s ⬆ 0.3kiB/s    
2023-05-13 23:40:18 [Relaychain] 💤 Idle (0 peers), best: #0 (0xcb14…d6d8), finalized #0 (0xcb14…d6d8), ⬇ 0.6kiB/s ⬆ 0.8kiB/s 
...
2023-05-14 00:00:30 [Relaychain] ✨ Imported #1153 (0xa53c…e944)    
2023-05-14 00:00:33 [Relaychain] 👴 Applying authority set change scheduled at block #1151    
2023-05-14 00:00:33 [Relaychain] 👴 Applying GRANDPA set change to new set [(Public(88dc3417d5058ec4b4503e0c12ea1a0a89be200fe98922423d4334014fa6b0ee (5FA9nQDV...)), 1), (Public(d17c2d7823ebf260fd138f2d7e27d114c0145d968b5ff5006125f2414fadae69 (5GoNkf6W...)), 1)]    
2023-05-14 00:00:34 [Relaychain] 💤 Idle (2 peers), best: #1153 (0xa53c…e944), finalized #1151 (0xded7…f559), ⬇ 0.9kiB/s ⬆ 0.6kiB/s    
2023-05-14 00:00:34 [Parachain] 💤 Idle (0 peers), best: #29 (0xa775…6eb3), finalized #29 (0xa775…6eb3), ⬇ 0 ⬆ 0    
2023-05-14 00:00:36 [Relaychain] ✨ Imported #1154 (0x4feb…441f)    
2023-05-14 00:00:36 [Parachain] Starting collation. relay_parent=0x4febb4a537a567d36ae0484b1451466cc59f8bd40743a1b015046f522a4d441f at=0x48b90cffc2d9851b763ef7b6372e908b757fc138a727ea08b28f6bf633ca082b
2023-05-14 00:00:39 [Relaychain] 💤 Idle (2 peers), best: #1154 (0x4feb…441f), finalized #1151 (0xded7…f559), ⬇ 1.0kiB/s ⬆ 0.7kiB/s    
2023-05-14 00:00:39 [Parachain] 💤 Idle (0 peers), best: #30 (0x48b9…082b), finalized #29 (0xa775…6eb3), ⬇ 49 B/s ⬆ 46 B/s    
2023-05-14 00:00:42 [Relaychain] ✨ Imported #1155 (0x1020…4ba9)    
2023-05-14 00:00:42 [Parachain] Starting collation. relay_parent=0x102066447990032d561b41002fb92a8b753745b5bacdd5ded6c9d97c64964ba9 at=0x48b90cffc2d9851b763ef7b6372e908b757fc138a727ea08b28f6bf633ca082b
2023-05-14 00:00:44 [Relaychain] 💤 Idle (2 peers), best: #1155 (0x1020…4ba9), finalized #1152 (0x42ee…81a5), ⬇ 0.8kiB/s ⬆ 0.5kiB/s    
2023-05-14 00:00:44 [Parachain] 💤 Idle (0 peers), best: #30 (0x48b9…082b), finalized #29 (0xa775…6eb3), ⬇ 24 B/s ⬆ 24 B/s    
2023-05-14 00:00:48 [Relaychain] ✨ Imported #1156 (0x25f9…a4e0)    
2023-05-14 00:00:48 [Parachain] Starting collation. relay_parent=0x25f9fd290b7f6bce0da53a72e86abe9ac1948e3b0d6bca61a964af01889fa4e0 at=0x48b90cffc2d9851b763ef7b6372e908b757fc138a727ea08b28f6bf633ca082b
2023-05-14 00:00:48 [Parachain] 🙌 Starting consensus session on top of parent 0x48b90cffc2d9851b763ef7b6372e908b757fc138a727ea08b28f6bf633ca082b    
2023-05-14 00:00:48 [Parachain] 🎁 Prepared block for proposing at 31 (1 ms) [hash: 0x02df3f9bf37554c7aea3106930f79187dc508c0a8acbd6867e54149ec1919264; parent_hash: 0x48b9…082b; extrinsics (2): [0x3838…32d0, 0x0492…404b]]    
2023-05-14 00:00:48 [Parachain] 🔖 Pre-sealed block for proposal at 31. Hash now 0xef71484dad41ec965d101e1e130a7a09fa468c0f9f753a5afc1d7959036b75fd, previously 0x02df3f9bf37554c7aea3106930f79187dc508c0a8acbd6867e54149ec1919264.    
2023-05-14 00:00:48 [Parachain] ✨ Imported #31 (0xef71…75fd)    
2023-05-14 00:00:48 [Parachain] PoV size { header: 0.1787109375kb, extrinsics: 2.7470703125kb, storage_proof: 2.876953125kb }
2023-05-14 00:00:48 [Parachain] Compressed PoV size: 5.150390625kb
2023-05-14 00:00:48 [Parachain] Produced proof-of-validity candidate. block_hash=0xef71484dad41ec965d101e1e130a7a09fa468c0f9f753a5afc1d7959036b75fd
2023-05-14 00:00:49 [Relaychain] 💤 Idle (2 peers), best: #1156 (0x25f9…a4e0), finalized #1153 (0xa53c…e944), ⬇ 1.1kiB/s ⬆ 1.7kiB/s    
2023-05-14 00:00:49 [Parachain] 💤 Idle (0 peers), best: #30 (0x48b9…082b), finalized #29 (0xa775…6eb3), ⬇ 0 ⬆ 0    
2023-05-14 00:00:54 [Relaychain] ✨ Imported #1157 (0x099c…38a7)    
2023-05-14 00:00:54 [Relaychain] 💤 Idle (2 peers), best: #1157 (0x099c…38a7), finalized #1154 (0x4feb…441f), ⬇ 1.2kiB/s ⬆ 0.7kiB/s    
2023-05-14 00:00:54 [Parachain] 💤 Idle (0 peers), best: #30 (0x48b9…082b), finalized #30 (0x48b9…082b), ⬇ 46 B/s ⬆ 49 B/s    
2023-05-14 00:00:59 [Relaychain] 💤 Idle (2 peers), best: #1157 (0x099c…38a7), finalized #1155 (0x1020…4ba9), ⬇ 0.5kiB/s ⬆ 0.4kiB/s    
2023-05-14 00:00:59 [Parachain] 💤 Idle (0 peers), best: #30 (0x48b9…082b), finalized #30 (0x48b9…082b), ⬇ 24 B/s ⬆ 24 B/s    
2023-05-14 00:01:00 [Relaychain] ✨ Imported #1158 (0x431b…4aa3)    
2023-05-14 00:01:00 [Parachain] Starting collation. relay_parent=0x431ba7328819ee5e2931c691e839e6cfa26895609a325029d1a95d575b8e4aa3 at=0xef71484dad41ec965d101e1e130a7a09fa468c0f9f753a5afc1d7959036b75fd
2023-05-14 00:01:04 [Relaychain] 💤 Idle (2 peers), best: #1158 (0x431b…4aa3), finalized #1155 (0x1020…4ba9), ⬇ 0.8kiB/s ⬆ 0.6kiB/s    
2023-05-14 00:01:04 [Parachain] 💤 Idle (0 peers), best: #31 (0xef71…75fd), finalized #30 (0x48b9…082b), ⬇ 0 ⬆ 0    
2023-05-14 00:01:04 [Parachain] expired: 12D3KooWMVDkjLYCuRQvKbgtQoqoaNe5CC5x6Jh9M84tfyHPvEs3 /ip4/192.168.49.1/tcp/30334    
2023-05-14 00:01:04 [Parachain] expired: 12D3KooWMVDkjLYCuRQvKbgtQoqoaNe5CC5x6Jh9M84tfyHPvEs3 /ip4/10.42.0.0/tcp/30334    
2023-05-14 00:01:09 [Relaychain] 💤 Idle (1 peers), best: #1158 (0x431b…4aa3), finalized #1156 (0x25f9…a4e0), ⬇ 0.5kiB/s ⬆ 0.3kiB/s    
2023-05-14 00:01:09 [Parachain] 💤 Idle (0 peers), best: #31 (0xef71…75fd), finalized #30 (0x48b9…082b), ⬇ 24 B/s ⬆ 24 B/s    
2023-05-14 00:01:14 [Relaychain] 💤 Idle (0 peers), best: #1158 (0x431b…4aa3), finalized #1156 (0x25f9…a4e0), ⬇ 24 B/s ⬆ 0.1kiB/s    
2023-05-14 00:01:14 [Parachain] 💤 Idle (0 peers), best: #31 (0xef71…75fd), finalized #30 (0x48b9…082b), ⬇ 24 B/s ⬆ 24 B/s   
```
</details>


**Now we have working parachain and that is producing blocks and we can also do the transactions.**

- Parachain created and running at ParaID: 2000\
![Parachain Created](./home/yasin/Pictures/Screenshots/parachain-created.png)
- Parachain block information \
![Block Information](./home/yasin/Pictures/Screenshots/parachain-block-info.png)
- Parachain transaction information \
![Trasaction Information](./home/yasin/Pictures/Screenshots/parachain-transaction.png)


## Resources
- [Substrate Documentation](https://substrate.dev/)
- [Cumulus Documentation](https://github.com/paritytech/cumulus)
- [Polkadot Wiki](https://wiki.polkadot.network/)
- [Polkadot GitHub Repository](https://github.com/paritytech/polkadot)
