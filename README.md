# Bitcoin Testnet Wallet Generator

This project demonstrates how to generate a Bitcoin Testnet wallet using bip32, bip39, and bitcoinjs-lib. It includes generating a mnemonic phrase, creating a seed, and deriving a Bitcoin address and private key.

# Pre-requisites

Ensure you have Node.js installed on your machine. This project was developed using Node.js v18.19.0.

# Installation

1. Clone the repository:

```
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
```

2. Install the necessary dependencies:

```
npm install
```

# Usage

Run the script to generate a new Bitcoin Testnet wallet:

```
npm start
```

# Output

The script will output a new seed, node private key, and the corresponding Bitcoin Testnet address. Example output:

{
address: <your generated address>,
privateKey: <your generated private key>,
seed: <your generated seed>'
}

# Troubleshooting

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

# License

This project is licensed under the MIT License. See the LICENSE file for details.
