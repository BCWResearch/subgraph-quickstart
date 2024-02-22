# subgraph-quickstart

This is a quickstart for deploying a subgraph using Arkhia's subgraph template.

Docs: [https://docs.arkhia.io/quickstart/subgraph](https://docs.arkhia.io/docs/arkhia-api/subgraph-api/subgraph.quickstart)

## Getting Started

### 1. Update the Environment Variables

Update the `.env` file with the API endpoint and API key you copied from the Arkhia Dashboard.

```bash
cp .env.example .env
```

Your `.env` file should look something like this:

```bash
# .env
SUBGRAPH_ENDPOINT=https://starter.arkhia.io/hedera/mainnet/subgraph/v1
API_KEY=YOUR_API_KEY
IPFS_ENDPOINT=https://starter.arkhia.io/hedera/mainnet/ipfs/v1

# SubGraph Config
GRAPH_CONTRACT_ADDRESS=0x00000000000000000000000000000000000bf929
GRAPH_START_BLOCK=59288563
GRAPH_NETWORK=mainnet
SUBGRAPH_NAME=erc20-transfers-quickstart
```

### 2. Deploy the Subgraph

```bash
npm install
npm run compile
npm run create
```

Once the subgraph is created, you will see the subgraph in the Arkhia Dashboard under the Subgraph section.

Now, deploy the subgraph to the Arkhia infrastructure.

```bash
npm run deploy
```

<details close>
<summary> Troubleshooting </summary>

    If you don't see the IPFS endpoint under Arkhia Dashboard, you can use the subgraph endpoint as the IPFS endpoint with minor changes by replacing `subgraph` with `ipfs` in the URL.
        - Example: `https://starter.arkhia.io/hedera/mainnet/subgraph/v1` -> `https://starter.arkhia.io/hedera/mainnet/ipfs/v1`

</details>

