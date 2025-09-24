# Base Simple Marketplace

This repository contains a simple ERC20-based marketplace smart contract that can be deployed on the **Base Network** using Remix IDE. Users can list items for sale and others can buy them using a specific ERC20 token.

---

## 1. Open Remix IDE

- Go to [https://remix.ethereum.org](https://remix.ethereum.org)  
- Connect your wallet (e.g., MetaMask) to Base Testnet or Mainnet.

---

## 2. Create Contract File

- File path: `contracts/Marketplace.sol`  
- Paste the smart contract code from `Marketplace.sol`.

---

## 3. Compile Contract

- Solidity compiler: **0.8.13**  
- Enable optimization (optional)  
- Click **Compile Marketplace.sol**  

> Ensure there are no compilation errors.

---

## 4. Deploy Contract

- Environment: **Injected Web3**  
- Network: Base Testnet/Mainnet  
- Constructor parameter: ERC20 token address (used for payment)  
- Click **Deploy** and confirm in your wallet

---

## 5. Interact with Contract

### List Item
- `listItem(price)` → List an item for sale  
  - `price` is in ERC20 token units (check decimals of your token)  
  - Returns `itemId`  

### Buy Item
- `buyItem(itemId)` → Buy an item listed  
  - Ensure you `approve` the Marketplace contract to spend your ERC20 tokens first  

### Admin Functions
- `withdrawTokens(amount)` → Owner can withdraw any tokens from the contract  

---

## Notes

- Each item is tracked by `itemId`.  
- Items cannot be bought twice.  
- For production, consider adding:  
  - NFT/asset integration  
  - Fees for marketplace owner  
  - Enhanced security checks  

