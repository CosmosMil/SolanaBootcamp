# SolanaBootcamp

# SolanaBootcamp

> **Note**: We're expecting you have both [`rust`](https://www.rust-lang.org/tools/install) and [`solana cli`](https://docs.solana.com/cli/install-solana-cli-tools) installed. If you are running on the MacOS M1 and encounter issues, we suggest **NOT** to use brew to install rust, instead use curl or install from source.

1. Install and build - commands builds binary files for each of the examples and creates `target/` directory within `examples_baremtal/`

   ```zsh
   npm i
   npm run build
   ```

1. Set your config to localhost

   ```zsh
   solana config set --url localhost
   ```

1. Then run in seperate terminal window - will spin up local solana cluster for you with RPC enpoint defaulted to `localhost:8899` npm run script 'start-local-cluster' is invoking `solana-test-validator --reset`

   ```zsh
   npm run start-local-cluster
   ```

1. You can monitor the logs in seperate window by running

   ```zsh
    solana logs
   ```

## Commans for each example

1. For each example run the following commands, the program would be deployed to the network specified in solana config

   ```zsh
   npm run deploy:n
   ```

   > where `n` is example number from 1 to 7 what this script does in the background `solana program deploy ./examples_baremetal/target/deploy/nameOfExampleProgram.so`

1. To interact with the contract, we'll be running the typescript code located in `client/` within each example

   ```zsh
   npm run call:n
   ```

   > where n is example number from 1 to 8

## Devnet

1. If you want to use devnet run:

   ```zsh
   solana config set --url https://api.devnet.solana.com

   # or

   solana config set --url devnet
   ```
