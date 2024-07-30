# How To use an External Bitcoind Server on Umbrel

## First Backup your Files
1. Access Umbrel via SSH
2. Go to `~/umbrel/app-data/bitcoin` and backup the files
   ```
   cp .env .env-bck
   cp exports.sh exports.bck
   cp docker-compose.yml docker-compose.bck
## Edit the Files with the Changes Below
1. `.env`
   ```
   export APP_BITCOIN_NETWORK='mainnet'
   export APP_BITCOIN_RPC_USER='your_rpc_user'
   export APP_BITCOIN_RPC_PASS='your_rpc_pass'
   export APP_BITCOIN_RPC_AUTH='your_rpc_user:your_rcp_pass'

2. `exports.sh`
   Replace the file for this one
   [exports.sh](https://github.com/jvxis/nr-tools/blob/main/external_bitcoin/exports.sh)

3. `docker-compose.yml'
   Replace the file for this one
   [docker-compose.yml](https://github.com/jvxis/nr-tools/blob/main/external_bitcoin/docker-compose.yml)
   And replace the lines 20 to 23 with your rpc credentials
   ```
   RPC_USER: your_rpc_user
   BITCOIN_RPC_USER: your_rpc_user
   RPC_PASSWORD: your_rpc_pass
   BITCOIN_RPC_PASSWORD: your_rpc_pass

