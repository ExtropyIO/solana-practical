### Installing Solana  Command Line Tools

You can either install the tools locally, or use the gitpod environment 
The instructions are also given in the [documenttion](https://docs.solana.com/cli/install-solana-cli-tools)

### Mac / Linux
`sh -c "$(curl -sSfL https://release.solana.com/v1.10.8/install)"`

You need to follow the instructions about updating the PATH variable, you can check the installation with 
`solana --version`

### Windows 
Open a command prompt as an administrator
Run
`curl https://release.solana.com/v1.10.8/solana-install-init-x86_64-pc-windows-msvc.exe --output C:\solana-install-tmp\solana-install-init.exe --create-dirs`

`C:\solana-install-tmp\solana-install-init.exe v1.10.8`

Close and re open the command prompt, this time as a normal user
Check the installation with 
`solana --version`

--- 

To get help run
`solana --help`

Create a keypair
`mkdir ~/my-solana-wallet`
`solana-keygen new --outfile ~/my-solana-wallet/my-keypair.json`

display the result with
`solana-keygen pubkey ~/my-solana-wallet/my-keypair.json`

verify your address
`solana-keygen verify <PUBKEY> ~/my-solana-wallet/my-keypair.json`

### Connect to the dev network
`solana config set --url https://api.devnet.solana.com`
You can check the configuration with
`solana config get`

Get some tokens from dev net
`solana airdrop 1 <RECIPIENT_ACCOUNT_ADDRESS> --url https://api.devnet.solana.com`

you will receive the transaction ID, and can look for this on the  [dev net block explorer](https://explorer.solana.com/?cluster=devnet)

You can also check your balance with 
`solana balance <ACCOUNT_ADDRESS> --url https://api.devnet.solana.com`
