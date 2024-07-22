# SATS chain
Both **sats** and **bevm** chains are blockchains built based on **bevm-stack** technology. 
They have the same source code but different configurations.

# Run sats archive node
[Download the latest stable release of the SATS node](../binary) from the builds repo and unpack. 
Make sure you're running the Ubuntu system. 
Choose the corresponding binary package according to your 
operating system architecture here.

```bash
$ bevm --version
bevm 0.1.9-ec0f0b31fbe
```

Replace 'your-node-name' with a unique name for your node.
```bash
$ bevm --chain=sats \
    -d data \
    --pruning=archive \
    --name "your-node-name" \
    --rpc-port 8087 \
    --rpc-cors all \
    --rpc-max-connections 100000
```

When you initiate a SATS archive node, opening a WS/HTTP endpoint on port **8087**.