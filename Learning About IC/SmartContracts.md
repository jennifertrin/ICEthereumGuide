# 📜 Smart Contracts on Ethereum vs. ICP

Smart contracts are programs stored on the blockchain that run particular code when certain conditions are met. 

Smart contracts can create and distribute NFTs and tokens, and any transaction on the blockchain that you can think of.

Though the same smart contract functionality on Ethereum exists on the Internet Computer, this article acts as a guide to the different terminology and concepts used to describe smart contracts on both chains.

To start, here is a comparison between the terminology used to describe smart contracts and concepts related to them:

## **Terminology Comparer Overview**

| Ethereum | Internet Computer |
| --- | --- |
| Smart contract | Canister |
| Smart contract owner | Canister controller |
| Gas | Cycles |

We’ll cover how to create and use smart contracts, and their key differences on both chains. 

## 🪄 Creation

### How do you create a smart contract?

On **Ethereum**, a smart contract owner writes the code to the smart contract and deploys the smart contract onto the blockchain. 

On the **Internet Computer**, a developer creates the canister (or smart contract) and then installs or writes code in the canister. 

### What languages can you write your smart contract?

On **Ethereum**, you must write your smart contract in Solidity.

On the **Internet Computer**, you can write your smart contract on Rust, Typescript, Mokoto, Python, or any other language that can be compiled on WASM.

### How do you update a smart contract?

On **Ethereum**, smart contracts are immutable and therefore, are not changeable. Companies and individuals looking to update their smart contracts must create new smart contracts and migrate all of their content to the new smart contract.

The old, unused smart contracts are still listed on the chain and can be used by users. 

On the **Internet Computer**, you can create a non-upgradable or an upgradable canister. A non-upgradable canister will not have a controller or smart contract owner and is immutable, similar to Ethereum smart contracts. 

Upgradable contracts are assigned to a list of controller(s) or owner(s). The controller(s) can update the canister by reinstalling the code or updating the canister to a new version.

The previous canister is completely overwritten if you reinstall the code. Users cannot utilize old functions with a reinstall. 

The previous canister can preserve its previous state with an update. Users can utilize old and new functions. 

A controlled can also delete the previous canister completely. 

```markdown
💡 Woah, a controller or smart contract owner can completely overwrite a smart contract? As an Ethereum user, you might ask these questions:

How do I trust the controller? How do I prevent getting rugged or hacked?

Canisters can forgo a controller and the ability for updates. 

Canisters should look to decentralize their ownership. Canisters can be controlled by SNS or a DAO that makes sure that the canister is not updated or reinstalled with malicious code. 

On the other hand, canisters on the Internet Computer are well-configured to enable a group of people such as a DAO to control their updates. 

To learn more, check here: https://internetcomputer.org/docs/current/concepts/trust-in-canisters
```

```markdown
💡  What happens to my NFTs or tokens if a canister is deleted?

Your NFTs and tokens will be deleted as well. DAOs should ideally govern canisters with the NFT or token registry to prevent this from happening. 

On the other hand, forks and migrations are easier to maintain. Has any of your users sent tokens to a depreciated contract or missed a deadline to convert a new version of a token? Your team will not need to worry about users making transactions to a deprecated contract.
```

### Is there a testing environment?

On **Ethereum**, you can write and deploy your smart contract on a test environment or "testnet". Once you are done with testing, you can deploy your final smart contract onto the main environment or "mainnet."

Developers discovering bugs in smart contracts deployed on mainnet is evitable even with a testing environment. 

On the **Internet Computer**, you can test your canister in your local environment. We are looking to launch a playground that further helps developers with testing. Given that all deployed contracts reside on the mainnet, the capability to upgrade and delete contracts becomes essential.

## 🔍 Utilization

### How do you use a smart contract?

On **Ethereum**, users make requests to a smart contract. Most commonly, users use a website that is connected to a smart contract (i.e. NFT marketplace). When they interact with the website to purchase or transfer an NFT or token, they are utilizing the smart contract to do so.

Users must pay a fee or “gas” to make a request to a smart contract.

On the **Internet Computer**, users also make requests to a canister, most commonly using a web interface that is connected to the canister. However, the user is not expected to pay for cycles or gas as the canister would pay for the cycles.

```markdown
💡 How would I prevent bots or malicious actors from using my canister and depleting my cycle or gas funds?

You can require authentication to access certain or all functions. 
```

```markdown
💡 What happens when my cycle funds run out considering users do not pay for cycles or gas?

Tools such as CycleOps (https://cycleops.dev/) can automate the top-up of your cycles. 

You can also set an initial cap in your canister to make sure that your canister is not available once it hits a certain threshold. 

Other canisters can accept cycles from other canisters. This enables smart contracts or canisters to form more trusted, partnerships with each other.
```

On the **Internet Computer**, canisters function as versatile full-service programs. Developers can opt for hybrid approach by keeping certain smart contracts on Ethereum while leveraging ICP canisters to implement other functionalities.

In future sections, we will provide examples of when you can use both Ethereum smart contracts and ICP canisters. 