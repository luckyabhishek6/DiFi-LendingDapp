- SmartContract link--> https://github.com/luckyabhishek6/DeFi-Lending-Borrowing-Smart-Contract-.git

- vist Lending Dapp -->  https://difi-lendingdapp.vercel.app/

# Borrowing and Lending Decentralized Aapplication

Decentralized finance, also known as DeFi, uses cryptocurrency and blockchain technology to manage financial transactions. DeFi aims to democratize finance by replacing legacy, centralized institutions with peer-to-peer relationships that can provide a full spectrum of financial services, from everyday banking, loans and mortgages, to complicated contractual relationships and asset trading.

“Decentralized finance is an unbundling of traditional finance,” says Rafael Cosman, CEO and co-founder of TrustToken. “DeFi takes the key elements of the work done by banks, exchanges and insurers today—like lending, borrowing and trading—and puts it in the hands of regular people.”


![Screenshot (221)](https://user-images.githubusercontent.com/41932087/192129171-a54973da-5709-4477-9403-2834bee98bf1.png)


- `Warning!`Ropsten network and this faucet will be shut down in Oct 2022.
More info in  Ethereum Foundation blog (https://blog.ethereum.org/2022/09/09/kiln-shutdown).


![Screenshot (222)](https://user-images.githubusercontent.com/41932087/192129187-b6445a12-f367-4be5-81b5-0c457e34607f.png)

## Prerequisites
-  Make a fork of this repository and clone it to your machine.
-  Make sure you use at least version of Node.js.
-  To install Node.JS as a Windows user, download the required installation from the Node.js website.
-  To reset the older Node.JS installation so that you can upgrade to version
-  Metamask extenstion its is required.


## Procedure 

* Navigate to your cloned repository  and install the `npm tool`:

```
npm install
```

Dependecies packages will be downloaded.

* Start DApp on localhost server:

```
start run dev
```


* For a production build:

```
npm dev  build
```

# hardhat configuration

The project folder will contain a `hardhat.config.js` file which is the configuration file, located at the root of the project directory.

```
require("@nomiclabs/hardhat-waffle");
require("@nomiclabs/hardhat-etherscan");
require('dotenv').config({path:'./.env.local'});

task("accounts", "Prints the list of accounts", async(taskArgs, hre) => {
    const accounts = await hre.ethers.getSigners();

    for (const account of accounts) {
        console.log(account.address);
    }
});
const privateKey= process.env.NEXT_PUBLIC_PRIVATE_KEY
module.exports = {
    solidity: "0.8.4",
    networks: {
        goerli: {
            url:process.env.NEXT_PUBLIC_RPC_URL,
            accounts: [privateKey],
        },
    },
    etherscan: {
        apiKey: "YWN2M9EMSYSQKIHNC1NBAK39KF53GHRN**",
    },
};

```

## Functionality
- Lending order 
- Borrow request
- Loan payback 
- Withdraw

## Description
- The loan contract only deployed to Ropsten testnet.
- This platform only supported lucky token and ETH.

- `Warning!`Ropsten network and this faucet will be shut down in Oct 2022.
More info in  Ethereum Foundation blog (https://blog.ethereum.org/2022/09/09/kiln-shutdown).
- Successfully verified contract Loan on Etherscan.
https://ropsten.etherscan.io/address/0x682438317a94cE9bB31915Bda482bb2F5001545F#code 

## Tech/Framework used
- [x] Solidity -> contract writing 
- [x] harthat -> ethereum development environment
- [x] React
- [x] Vite
- [x] Ethers.js
- [x] Tailwindcss
