Bitcoin Testnet Wallet Generator
This project demonstrates how to generate a Bitcoin Testnet wallet using bip32, bip39, and bitcoinjs-lib. It includes generating a mnemonic phrase, creating a seed, and deriving a Bitcoin address and private key.

Pre-requisites
Ensure you have Node.js installed on your machine. This project was developed using Node.js v18.19.0.

Installation
Clone the repository:

```
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
Install the necessary dependencies:
```

npm install
Usage
Run the script to generate a new Bitcoin Testnet wallet:

```
npm start
```

Output
The script will output a new mnemonic phrase, seed, root key, account key, node public key, node private key, and the corresponding Bitcoin Testnet address. Example output:

plaintext
Mnemonic: wide news check sound muscle stock roof summer meadow lazy grant fox
Seed: 27d28f461cea290b88a3f6cdc5cf2a19319243c8e8aae4413afaf6753855e4615202578441acc5ef99c16e89a02bf51df80bb0b3ebecf4deabb1facfa32780a6
Root Key: tprv8ZgxMBicQKsPdH7L3nLAc1hqggDAWjLNVwZ2qnQupSfrmiWtMVPhwkdzAxdVFpr2YFFDBwJfdxUfJTs1GZfRZfWM4pyLKeXvGYmUCd6ehBc
Account Key: tprv8hgpDrDPZh5xANYwfNKixrArVi6As2cYUBmatHrraRVRJFEv8MszJcm4F6uwvkaQx4zVxCZDim2Y9vBFgB7qYe4U5DgbYaNADTxBb9FvGMe
Node Public Key: 022518ab4d28e0f593b1e6bf683efe3ab1f4a88940d13e70736dd74597aca9e16d
Node Private Key: cVt8CA7ZS22pvuPubmgFikX8H4omUVXeaR2BCXuxMg2HimWtsokf
Bitcoin Address: <your generated address>
Troubleshooting
If you encounter the error TypeError: Not enough data:

Ensure you are passing the publicKey as a Buffer to the bitcoin.payments.p2pkh function:

```
let btcAddress = bitcoin.payments.p2pkh({
pubkey: Buffer.from(node.publicKey),
network: network,
}).address;
```

Verify the versions of your dependencies. You may need to update bitcoinjs-lib:

```
npm install bitcoinjs-lib@latest
```

License
This project is licensed under the MIT License. See the LICENSE file for details.
