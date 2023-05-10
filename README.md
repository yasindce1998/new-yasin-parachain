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
```sh
➜  ~ substrate-benchmark-machine
[INFO] Performing quick hardware check...
[INFO] 🏁 CPU score: 731.75 MiBs (❌ Blake2256: expected minimum 1.00 GiBs)
[INFO] 🏁 Memory score: 7.39 GiBs (❌ MemCopy: expected minimum 14.32 GiBs)
[INFO] 🏁 Disk score (seq. writes): 71.13 MiBs (❌ DiskSeqWrite: expected minimum 450.00 MiBs)
[INFO] 🏁 Disk score (rand. writes): 33.14 MiBs (❌ DiskRndWrite: expected minimum 200.00 MiBs)
[INFO] ⚠  The hardware does not meet the minimal requirements for role 'Authority'.
```

## To Build this project
```sh
git clone https://github.com/yasindce1998/new-yasin-parachain.git
cd new-yasin-parachain
cargo build --release
```
This will take some time to build and after finish building the project.

```sh
./target/release/parachain-template-node --help
```
Run this command to make sure if your build is built correctly.

After that execute the binary
```shell
./target/release/parachain-template-node --dev
```

<details>
  <summary>Output</summary>

```sh
➜  new-yasin-parachain git:(main) ✗ ./target/release/parachain-template-node --dev
2023-05-10 20:50:14 Parachain Collator Template    
2023-05-10 20:50:14 ✌️  version 0.1.0-ebbed24a0f6    
2023-05-10 20:50:14 ❤️  by Anonymous, 2020-2023    
2023-05-10 20:50:14 📋 Chain specification: Development    
2023-05-10 20:50:14 🏷  Node name: waiting-girl-6213    
2023-05-10 20:50:14 👤 Role: AUTHORITY    
2023-05-10 20:50:14 💾 Database: RocksDb at /tmp/substrateaUyboa/chains/dev/db/full    
2023-05-10 20:50:14 ⛓  Native runtime: template-parachain-1 (template-parachain-0.tx1.au1)    
2023-05-10 20:50:20 assembling new collators for new session 0 at #0    
2023-05-10 20:50:20 assembling new collators for new session 1 at #0    
2023-05-10 20:50:20 Parachain id: Id(1000)    
2023-05-10 20:50:20 Parachain Account: 5Ec4AhPZk8STuex8Wsi9TwDtJQxKqzPJRCH7348Xtcs9vZLJ    
2023-05-10 20:50:20 Parachain genesis state: 0x000000000000000000000000000000000000000000000000000000000000000000495b11519ee6f00256228938d18b6fb21b63d9c5b31c6469c6baf4b4b183ed3c03170a2e7597b7b7e3d84c05391d139a62b157e78786d8c082f29dcf4c11131400    
2023-05-10 20:50:20 Is collating: yes    
2023-05-10 20:50:22 [Parachain] assembling new collators for new session 0 at #0    
2023-05-10 20:50:22 [Parachain] assembling new collators for new session 1 at #0    
2023-05-10 20:50:24 [Parachain] 🔨 Initializing Genesis block/state (state: 0x495b…ed3c, header-hash: 0xb3de…2dc8)    
2023-05-10 20:50:29 [Relaychain] Took active validators from set with wrong size    
2023-05-10 20:50:29 [Relaychain] Took active validators from set with wrong size    
2023-05-10 20:50:29 [Relaychain] Took active validators from set with wrong size.    
2023-05-10 20:50:29 [Relaychain] Took active validators from set with wrong size    
2023-05-10 20:50:34 [Relaychain] 🔨 Initializing Genesis block/state (state: 0x50a1…c130, header-hash: 0xd476…b2b5)    
2023-05-10 20:50:34 [Relaychain] 👴 Loading GRANDPA authority set from genesis on what appears to be first startup.    
2023-05-10 20:50:40 [Relaychain] 👶 Creating empty BABE epoch changes on what appears to be first startup.    
2023-05-10 20:50:40 [Relaychain] 🏷  Local node identity is: 12D3KooWB93UdgGB2ZN8Dwn2dc9vttk5nbwpKPseHLun67oyag4c    
2023-05-10 20:50:41 [Relaychain] 💻 Operating system: linux    
2023-05-10 20:50:41 [Relaychain] 💻 CPU architecture: x86_64    
2023-05-10 20:50:41 [Relaychain] 💻 Target environment: gnu    
2023-05-10 20:50:41 [Relaychain] 💻 CPU: Intel(R) Core(TM) i5-5300U CPU @ 2.30GHz    
2023-05-10 20:50:41 [Relaychain] 💻 CPU cores: 2    
2023-05-10 20:50:41 [Relaychain] 💻 Memory: 7837MB    
2023-05-10 20:50:41 [Relaychain] 💻 Kernel: 5.19.0-38-generic    
2023-05-10 20:50:41 [Relaychain] 💻 Linux distribution: Ubuntu 22.04.2 LTS    
2023-05-10 20:50:41 [Relaychain] 💻 Virtual machine: no    
2023-05-10 20:50:41 [Relaychain] 📦 Highest known block at #0    
2023-05-10 20:50:41 [Relaychain] 〽️ Prometheus exporter started at 127.0.0.1:9616    
2023-05-10 20:50:41 [Relaychain] Running JSON-RPC HTTP server: addr=127.0.0.1:9934, allowed origins=["http://localhost:*", "http://127.0.0.1:*", "https://localhost:*", "https://127.0.0.1:*", "https://polkadot.js.org"]    
2023-05-10 20:50:41 [Relaychain] Running JSON-RPC WS server: addr=127.0.0.1:9945, allowed origins=["http://localhost:*", "http://127.0.0.1:*", "https://localhost:*", "https://127.0.0.1:*", "https://polkadot.js.org"]    
2023-05-10 20:50:41 [Relaychain] 🏁 CPU score: 896.34 MiBs    
2023-05-10 20:50:41 [Relaychain] 🏁 Memory score: 7.49 GiBs    
2023-05-10 20:50:41 [Relaychain] 🏁 Disk score (seq. writes): 72.08 MiBs    
2023-05-10 20:50:41 [Relaychain] 🏁 Disk score (rand. writes): 18.20 MiBs    
2023-05-10 20:50:41 [Relaychain] Starting with an empty approval vote DB.
2023-05-10 20:50:41 [Parachain] Using default protocol ID "sup" because none is configured in the chain specs    
2023-05-10 20:50:41 [Parachain] 🏷  Local node identity is: 12D3KooWETC3Mqx5CMKbEEFdu2SxTGr3xVMCBJ9t4JDS52eee5sK    
2023-05-10 20:50:41 [Parachain] 💻 Operating system: linux    
2023-05-10 20:50:41 [Parachain] 💻 CPU architecture: x86_64    
2023-05-10 20:50:41 [Parachain] 💻 Target environment: gnu    
2023-05-10 20:50:41 [Parachain] 💻 CPU: Intel(R) Core(TM) i5-5300U CPU @ 2.30GHz    
2023-05-10 20:50:41 [Parachain] 💻 CPU cores: 2    
2023-05-10 20:50:41 [Parachain] 💻 Memory: 7837MB    
2023-05-10 20:50:41 [Parachain] 💻 Kernel: 5.19.0-38-generic    
2023-05-10 20:50:41 [Parachain] 💻 Linux distribution: Ubuntu 22.04.2 LTS    
2023-05-10 20:50:41 [Parachain] 💻 Virtual machine: no    
2023-05-10 20:50:41 [Parachain] 📦 Highest known block at #0    
2023-05-10 20:50:41 [Parachain] 〽️ Prometheus exporter started at 127.0.0.1:9615    
2023-05-10 20:50:41 [Parachain] Running JSON-RPC HTTP server: addr=127.0.0.1:9933, allowed origins=["*"]    
2023-05-10 20:50:41 [Parachain] Running JSON-RPC WS server: addr=127.0.0.1:9944, allowed origins=["*"]    
2023-05-10 20:50:41 [Parachain] 🏁 CPU score: 896.34 MiBs    
2023-05-10 20:50:41 [Parachain] 🏁 Memory score: 7.49 GiBs    
2023-05-10 20:50:41 [Parachain] 🏁 Disk score (seq. writes): 72.08 MiBs    
2023-05-10 20:50:41 [Parachain] 🏁 Disk score (rand. writes): 18.20 MiBs    
2023-05-10 20:50:41 [Parachain] ⚠️  The hardware does not meet the minimal requirements for role 'Authority'.    
2023-05-10 20:50:46 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 0 ⬆ 0    
2023-05-10 20:50:46 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 0 ⬆ 0    
2023-05-10 20:50:51 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 0 ⬆ 0    
```
</details>


## Resources
- [Substrate Documentation](https://substrate.dev/)
- [Cumulus Documentation](https://github.com/paritytech/cumulus)
- [Polkadot Wiki](https://wiki.polkadot.network/)
- [Polkadot GitHub Repository](https://github.com/paritytech/polkadot)
