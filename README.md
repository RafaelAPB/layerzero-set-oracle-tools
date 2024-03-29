# LayerZeroV2 Oracle Setup

This tool sets up the Blockdaemon oracle for an Oapp.

### Requirements

This is a Typescript project. Npm as package manager and node. Tested with npm v10.2.4, node 21.5.0.

## Getting started
The Blockdaemon DVN currently supports the following chains:
| **Chain**                 | **Endpoint ID** | **Env variable NETWORK** | **Oracle Address**                         |
|---------------------------|-----------------|--------------------------|--------------------------------------------|
| Avalanche Fuji (testnet)  | 40106           | fuji                     | 0xe695699B08bdDd9922079332625e5Df265dEfA50 |
| Ethereum Goerli (testnet) | 40121           | goerli                   | 0xe695699B08bdDd9922079332625e5Df265dEfA50 |
| Polygon Mumbai (testnet)  | 40109           | mumbai                   | 0x3c2269811836af69497E5F486A85D7316753cf62 |


1. Install node 21.5.0.

2. Install the dependencies with `npm install`.

3. Copy the environment variables with `cp .env.example .env`.

4. Populate the variables, including your Blockdaemon API Key (BLOCKDAEMON_API_KEY), the private key that you will be using to sign transactions (PRIVATE_KEY), the address of your LayerZero v2 application (OAPP_ADDRESS) and the network you are operating on (NETWORK). Make sure to choose a supported network, according to the above table.

5. Set the target chain endpoint ID (TARGET_CHAIN_ENDPOINT_ID). Check the endpoints here: https://docs.layerzero.network/contracts/endpoint-addresses. For example,the endpoint ID for Goerli is `40121`and for Mumbai is `40109`.
6. Set the message library address (MESSAGE_LIB_ADDRESS). Libraries here: https://docs.layerzero.network/contracts/messagelib-addresses. For example, for Goerli, the version 2 (uln302) message library is `0xb3f5e2ae7a0a7c4abc809730d8e5699020f466ef`.

7. Run the main script with `ts-node main.ts`.

## FAQ

#### Which chains does this tool support?

A: This tool supports Blockdaemon-powered oracles, deployed at Fuji, Goerli, and Mumbai.
