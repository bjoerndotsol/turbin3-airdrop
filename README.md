# Link to transaction

https://explorer.solana.com/tx/5ASP95khJtreMjhsE2EwFv83FGk8JqHH5q28XbaZnSUjdP6XVm6M8ZGfGxSYesa8EJYd1E378XAKrFnpL6YTuvaz?cluster=devnet

# About this repository

This repository contains the homework for the [Bridge to Turbin3](https://www.risein.com/bootcamp-details/bridge-to-turbin3/) course from [risein.com](https://www.risein.com/).

## Structure

The repository consists of multiple files, that should be run in the right order to ensure that the files and accounts were created and there is nothing missing.

### 1. keygen.ts

Generates a keypair using the `@solana/web3.js` library and prints the public and private keys to the console. The secret key is displayed as a `Uint8Array`.

After running the command below, you should create a file dev-wallet.json and copy/paste the private key in there.

Please don't forget to add this file to you `.gitignore`, so that you don't push it into the repository by accident.

**Execution:**

```sh
yarn keygen
```

### 2. airdrop.ts

Airdrops SOL into your wallet.

**Execution:**

```sh
yarn airdrop
```

### 3. transfer.ts

Transfers a small amount of SOL to another wallet. I created a second file called `dev-wallet2.json` with structure below, but you can also remove it and just add a public key. The choice is yours.

**Execution:**

```sh
yarn transfer
```

### 4. enroll.ts

This is the final step. It:

- Takes the GitHub account name hardcoded in line 15.
- Writes it to the WBA program specified by the IDL in programs/wba_prereq.ts on devnet using the Anchor JS client.
- After completing the transaction, a link to the transaction is printed to the console.

**Execution:**

```sh
yarn enroll
```
