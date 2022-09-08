<p align="center">
  <a href="https://solana.com">
    <img alt="Solana" src="https://i.imgur.com/uBVzyX3.png" width="250" />
  </a>
</p>


# Windows Wsl2

Open powerShell
```bash
wsl --install
```
If you see the help text run wls --list --online to list available distros

Set default WSL version in powerShell
```bash
wsl --set-default-version 2
```

Install distro
```bash
wsl --install -d <distro Name>
 ```

Set default Linux distribution
```bash
wsl --set-default <Distribution Name>
```

Open Terminal Distro Linux
```bash
sudo apt update
```

Install Node:

Using Ubuntu
```bash 
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt-get install -y nodejs 
```

Using Debian
```bash 
curl -fsSL https://deb.nodesource.com/setup_16.x | bash -
apt-get install -y nodejs
```

Install typescript
```bash
sudo apt install node-typescript
```

Install Rust
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Install Solana
```bash
sh -c "$(curl -sSfL https://release.solana.com/v1.11.10/install)"
```
Accessing windows folders:
```bash
cd /mnt/c/Users/<Your User>/
```

Open VsCode
```bash
code .
```

More Details node: <link> https://github.com/nodesource/distributions/blob/master/README.md</link>

More Details Wsl Windows: <link> https://docs.microsoft.com/en-us/windows/wsl/basic-commands#install-a-specific-linux-distribution</link>

# Linux
## Install Curl
```bash
sudo apt-get install curl
```

## Install Rust
```bash
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

## Install Node
```bash 
sudo apt-get install nodejs
```

## Install Npm
```bash
sudo apt-get install npm 
```

## Install solana and Solana-cli
```bash
sh -c "$(curl -sSfL https://release.solana.com/LATEST_RELEASE/install)"
```

## Verify version
```bash
solana --version
```

```bash
rust --version
```

```bash
node --version
```

## Comands Solana
<hr>

Set Localhost
```bash
solana config set --url http://127.0.0.1:8899
```

Create keypair id
```bash
solana-keygen new --outfile <CAMINHO-ABSOLUTO>/id.json
```

Set keypair
```bash
solana config set --keypair <CAMINHO-ABSOLUTO>/id.json
```

Get Public Key
```bash
solana-keygen pubkey
```

Airdrop
```bash
solana airdrop 1
```
Output:
```bash 
Requesting airdrop of 1 SOL
Signature: 21DNXkGKrTozs5MfdXy36oZz3g6EtBQL7c7nSy7yKiS9mKj1bFJ7oJPdWYgNhqmkWEwu33RJZGuofqVXyj1mDNE3
1 SOL
```

Balance:
```bash
solana balance
```

Confirm data localhost
```bash
solana config get
```


## Install Dependencies

```bash
npm install
```


## Execute Setup
<hr>

```bash
solana-test-validator
```

In another terminal: 
<hr>

```bash
tsc -p ./tsconfig.json
```

```bash
npm run && node build/setup.js
```

```bash
npm run && node build/investor.js
```

```bash
npm run && node build/breeder.js
```

```bash
npm run && node build/treasure.js
```

### All

```bash
npm run && node build/setup.js && node build/investor.js && node build/breeder.js && node build/treasure.js
```