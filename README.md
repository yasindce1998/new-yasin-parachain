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
./target/release/parachain-template-node
```
<details>
  <summary>Output</summary>

```sh
➜  release git:(main) ./parachain-template-node       
2023-05-10 11:37:09 Parachain Collator Template    
2023-05-10 11:37:09 ✌️  version 0.1.0-ebbed24a0f6    
2023-05-10 11:37:09 ❤️  by Anonymous, 2020-2023    
2023-05-10 11:37:09 📋 Chain specification: Local Testnet    
2023-05-10 11:37:09 🏷  Node name: depressed-chickens-9486    
2023-05-10 11:37:09 👤 Role: FULL    
2023-05-10 11:37:09 💾 Database: RocksDb at /home/yasin/.local/share/parachain-template-node/chains/local_testnet/db/full    
2023-05-10 11:37:09 ⛓  Native runtime: template-parachain-1 (template-parachain-0.tx1.au1)    
2023-05-10 11:37:14 assembling new collators for new session 0 at #0    
2023-05-10 11:37:14 assembling new collators for new session 1 at #0    
2023-05-10 11:37:14 Parachain id: Id(1000)    
2023-05-10 11:37:14 Parachain Account: 5Ec4AhPZk8STuex8Wsi9TwDtJQxKqzPJRCH7348Xtcs9vZLJ    
2023-05-10 11:37:14 Parachain genesis state: 0x000000000000000000000000000000000000000000000000000000000000000000495b11519ee6f00256228938d18b6fb21b63d9c5b31c6469c6baf4b4b183ed3c03170a2e7597b7b7e3d84c05391d139a62b157e78786d8c082f29dcf4c11131400    
2023-05-10 11:37:14 Is collating: no    
2023-05-10 11:37:17 [Parachain] assembling new collators for new session 0 at #0    
2023-05-10 11:37:17 [Parachain] assembling new collators for new session 1 at #0    
2023-05-10 11:37:19 [Parachain] 🔨 Initializing Genesis block/state (state: 0x495b…ed3c, header-hash: 0xb3de…2dc8)    
2023-05-10 11:37:24 [Relaychain] Took active validators from set with wrong size    
2023-05-10 11:37:24 [Relaychain] Took active validators from set with wrong size    
2023-05-10 11:37:24 [Relaychain] Took active validators from set with wrong size.    
2023-05-10 11:37:24 [Relaychain] Took active validators from set with wrong size    
2023-05-10 11:37:29 [Relaychain] 🔨 Initializing Genesis block/state (state: 0x50a1…c130, header-hash: 0xd476…b2b5)    
2023-05-10 11:37:29 [Relaychain] 👴 Loading GRANDPA authority set from genesis on what appears to be first startup.    
2023-05-10 11:37:34 [Relaychain] 👶 Creating empty BABE epoch changes on what appears to be first startup.    
2023-05-10 11:37:34 [Relaychain] 🏷  Local node identity is: 12D3KooWB2Gded7ujkgH3vYCXXQvmBtUTTmx68N9vP363EmvHBu7    
2023-05-10 11:37:35 [Relaychain] 💻 Operating system: linux    
2023-05-10 11:37:35 [Relaychain] 💻 CPU architecture: x86_64    
2023-05-10 11:37:35 [Relaychain] 💻 Target environment: gnu    
2023-05-10 11:37:35 [Relaychain] 💻 CPU: Intel(R) Core(TM) i5-5300U CPU @ 2.30GHz    
2023-05-10 11:37:35 [Relaychain] 💻 CPU cores: 2    
2023-05-10 11:37:35 [Relaychain] 💻 Memory: 7837MB    
2023-05-10 11:37:35 [Relaychain] 💻 Kernel: 5.19.0-38-generic    
2023-05-10 11:37:35 [Relaychain] 💻 Linux distribution: Ubuntu 22.04.2 LTS    
2023-05-10 11:37:35 [Relaychain] 💻 Virtual machine: no    
2023-05-10 11:37:35 [Relaychain] 📦 Highest known block at #0    
2023-05-10 11:37:35 [Relaychain] 〽️ Prometheus exporter started at 127.0.0.1:9616    
2023-05-10 11:37:35 [Relaychain] Running JSON-RPC HTTP server: addr=127.0.0.1:9934, allowed origins=["http://localhost:*", "http://127.0.0.1:*", "https://localhost:*", "https://127.0.0.1:*", "https://polkadot.js.org"]    
2023-05-10 11:37:35 [Relaychain] Running JSON-RPC WS server: addr=127.0.0.1:9945, allowed origins=["http://localhost:*", "http://127.0.0.1:*", "https://localhost:*", "https://127.0.0.1:*", "https://polkadot.js.org"]    
2023-05-10 11:37:35 [Relaychain] 🏁 CPU score: 841.58 MiBs    
2023-05-10 11:37:35 [Relaychain] 🏁 Memory score: 7.81 GiBs    
2023-05-10 11:37:35 [Relaychain] 🏁 Disk score (seq. writes): 60.70 MiBs    
2023-05-10 11:37:35 [Relaychain] 🏁 Disk score (rand. writes): 37.44 MiBs    
2023-05-10 11:37:35 [Relaychain] Starting with an empty approval vote DB.
2023-05-10 11:37:35 [Parachain] 🏷  Local node identity is: 12D3KooWMCkjCPiLWhxRiTzJ5ewoGFr3sXkrpuFWpckGUouXbPbF    
2023-05-10 11:37:35 [Parachain] 💻 Operating system: linux    
2023-05-10 11:37:35 [Parachain] 💻 CPU architecture: x86_64    
2023-05-10 11:37:35 [Parachain] 💻 Target environment: gnu    
2023-05-10 11:37:35 [Parachain] 💻 CPU: Intel(R) Core(TM) i5-5300U CPU @ 2.30GHz    
2023-05-10 11:37:35 [Parachain] 💻 CPU cores: 2    
2023-05-10 11:37:35 [Parachain] 💻 Memory: 7837MB    
2023-05-10 11:37:35 [Parachain] 💻 Kernel: 5.19.0-38-generic    
2023-05-10 11:37:35 [Parachain] 💻 Linux distribution: Ubuntu 22.04.2 LTS    
2023-05-10 11:37:35 [Parachain] 💻 Virtual machine: no    
2023-05-10 11:37:35 [Parachain] 📦 Highest known block at #0    
2023-05-10 11:37:35 [Parachain] 〽️ Prometheus exporter started at 127.0.0.1:9615    
2023-05-10 11:37:35 [Parachain] Running JSON-RPC HTTP server: addr=127.0.0.1:9933, allowed origins=["http://localhost:*", "http://127.0.0.1:*", "https://localhost:*", "https://127.0.0.1:*", "https://polkadot.js.org"]    
2023-05-10 11:37:35 [Parachain] Running JSON-RPC WS server: addr=127.0.0.1:9944, allowed origins=["http://localhost:*", "http://127.0.0.1:*", "https://localhost:*", "https://127.0.0.1:*", "https://polkadot.js.org"]    
2023-05-10 11:37:35 [Parachain] 🏁 CPU score: 841.58 MiBs    
2023-05-10 11:37:35 [Parachain] 🏁 Memory score: 7.81 GiBs    
2023-05-10 11:37:35 [Parachain] 🏁 Disk score (seq. writes): 60.70 MiBs    
2023-05-10 11:37:35 [Parachain] 🏁 Disk score (rand. writes): 37.44 MiBs    
2023-05-10 11:37:36 [Relaychain] discovered: 12D3KooWMCkjCPiLWhxRiTzJ5ewoGFr3sXkrpuFWpckGUouXbPbF /ip4/172.18.0.1/tcp/30333/ws    
2023-05-10 11:37:36 [Parachain] discovered: 12D3KooWB2Gded7ujkgH3vYCXXQvmBtUTTmx68N9vP363EmvHBu7 /ip4/192.168.49.1/tcp/30334/ws    
2023-05-10 11:37:36 [Parachain] discovered: 12D3KooWB2Gded7ujkgH3vYCXXQvmBtUTTmx68N9vP363EmvHBu7 /ip4/10.42.0.1/tcp/30334/ws    
2023-05-10 11:37:36 [Relaychain] discovered: 12D3KooWMCkjCPiLWhxRiTzJ5ewoGFr3sXkrpuFWpckGUouXbPbF /ip4/10.42.0.0/tcp/30333/ws    
2023-05-10 11:37:36 [Parachain] discovered: 12D3KooWB2Gded7ujkgH3vYCXXQvmBtUTTmx68N9vP363EmvHBu7 /ip4/10.42.0.0/tcp/30334/ws    
2023-05-10 11:37:36 [Parachain] discovered: 12D3KooWB2Gded7ujkgH3vYCXXQvmBtUTTmx68N9vP363EmvHBu7 /ip4/172.17.0.1/tcp/30334/ws    
2023-05-10 11:37:36 [Relaychain] discovered: 12D3KooWMCkjCPiLWhxRiTzJ5ewoGFr3sXkrpuFWpckGUouXbPbF /ip4/172.17.0.1/tcp/30333/ws    
2023-05-10 11:37:36 [Relaychain] discovered: 12D3KooWMCkjCPiLWhxRiTzJ5ewoGFr3sXkrpuFWpckGUouXbPbF /ip4/192.168.49.1/tcp/30333/ws    
2023-05-10 11:37:36 [Relaychain] discovered: 12D3KooWMCkjCPiLWhxRiTzJ5ewoGFr3sXkrpuFWpckGUouXbPbF /ip4/10.42.0.1/tcp/30333/ws    
2023-05-10 11:37:40 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 0.5kiB/s ⬆ 0.7kiB/s    
2023-05-10 11:37:40 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 0.7kiB/s ⬆ 0.5kiB/s    
2023-05-10 11:37:45 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 81 B/s ⬆ 79 B/s    
2023-05-10 11:37:45 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 79 B/s ⬆ 81 B/s    
2023-05-10 11:37:50 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 0 ⬆ 0    
2023-05-10 11:37:50 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 0 ⬆ 0    
2023-05-10 11:37:55 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 24 B/s ⬆ 24 B/s    
2023-05-10 11:37:55 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 24 B/s ⬆ 24 B/s    
2023-05-10 11:38:00 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 0 ⬆ 0    
2023-05-10 11:38:00 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 0 ⬆ 0    
2023-05-10 11:38:05 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 0 ⬆ 0    
2023-05-10 11:38:05 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 0 ⬆ 0    
2023-05-10 11:38:10 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 24 B/s ⬆ 24 B/s    
2023-05-10 11:38:10 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 24 B/s ⬆ 24 B/s    
2023-05-10 11:38:15 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 0 ⬆ 0    
2023-05-10 11:38:15 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 0 ⬆ 0    
2023-05-10 11:38:20 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 0 ⬆ 0    
2023-05-10 11:38:20 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 0 ⬆ 0    
2023-05-10 11:38:25 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 24 B/s ⬆ 21 B/s    
2023-05-10 11:38:25 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 21 B/s ⬆ 24 B/s    
2023-05-10 11:38:30 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 0 ⬆ 0    
2023-05-10 11:38:30 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 0 ⬆ 0    
2023-05-10 11:38:35 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 0 ⬆ 0    
2023-05-10 11:38:35 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 0 ⬆ 0    
2023-05-10 11:38:40 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 24 B/s ⬆ 24 B/s    
2023-05-10 11:38:40 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 24 B/s ⬆ 24 B/s    
2023-05-10 11:38:45 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 0 ⬆ 0    
2023-05-10 11:38:45 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 0 ⬆ 0    
2023-05-10 11:38:50 [Relaychain] 💤 Idle (0 peers), best: #0 (0xd476…b2b5), finalized #0 (0xd476…b2b5), ⬇ 0 ⬆ 0    
2023-05-10 11:38:50 [Parachain] 💤 Idle (0 peers), best: #0 (0xb3de…2dc8), finalized #0 (0xb3de…2dc8), ⬇ 0 ⬆ 0    
2023-05-10 11:38:54 Accepting new connection 1/100
```
</details>


## Resources
- [Substrate Documentation](https://substrate.dev/)
- [Cumulus Documentation](https://github.com/paritytech/cumulus)
- [Polkadot Wiki](https://wiki.polkadot.network/)
- [Polkadot GitHub Repository](https://github.com/paritytech/polkadot)
