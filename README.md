# kubo
Setup a local IPFS API Node to interact with the NFT marketplace

1-Download, install and run IPFS.

-Download and extract IPFS CLI (Kubo).

https://dist.ipfs.tech/#kubo

To show all the configuration JSON file in IPFS
```
ipfs config show
```

3-Using either shell/cmd/powershell, Navigate to the Kubo folder and enable CORS and API Access from any client.

Shell or CMD:
```shell
cd kubo
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin '[\"*\"]'
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods '[\"PUT\", \"GET\", \"POST\"]'
ipfs config --json Addresses.API \"/ip4/0.0.0.0/tcp/5001\"
```
For my particular Case using Powershell::
```shell
./ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin '[" "]'
./ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin '["*"]'
./ipfs config --json Addresses.API \"/ip4/0.0.0.0/tcp/5001\"
```

or other Powershell casses:
```shell
cd kubo
./ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin '[\"*\"]'
./ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods '[\"PUT\", \"GET\", \"POST\"]'
./ipfs config --json Addresses.API \"/ip4/0.0.0.0/tcp/5001\"
```

4- Restart IPFS.
