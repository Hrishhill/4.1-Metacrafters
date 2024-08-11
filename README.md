Certainly! Here's a highly professional README for your project:

---

# **HrishikeshSubnet: Custom Blockchain Subnet Setup & ERC20 Token Management**

## **Introduction**

Welcome to the HrishikeshSubnet project—a meticulously designed framework for setting up a custom blockchain subnet on the Avalanche network using Ubuntu via Windows Subsystem for Linux (WSL). This repository also includes a sophisticated ERC20 smart contract with minting and burning functionalities. By following this guide, you'll gain hands-on experience in deploying a private blockchain environment and interacting with it through MetaMask.

## **Table of Contents**

1. [Prerequisites](#prerequisites)
2. [Installation & Setup](#installation--setup)
   - [Step 1: UNIX User Setup & Avalanche CLI Installation](#step-1-unix-user-setup--avalanche-cli-installation)
   - [Step 2: HrishikeshSubnet Creation](#step-2-hrishikeshsubnet-creation)
   - [Step 3: Node Configuration](#step-3-node-configuration)
   - [Step 4: MetaMask Integration](#step-4-metamask-integration)
3. [Smart Contract Deployment](#smart-contract-deployment)
   - [Mint Function](#mint-function)
   - [Burn Function](#burn-function)
4. [Technical Considerations](#technical-considerations)
5. [Conclusion](#conclusion)
6. [Acknowledgments](#acknowledgments)
7. [License](#license)

## **Prerequisites**

Before proceeding, ensure that you have the following software installed and properly configured:

- **Windows Subsystem for Linux (WSL):** Ubuntu 20.04 LTS or later.
- **Avalanche CLI:** The command-line interface for subnet creation and management.
- **MetaMask:** A widely-used Ethereum wallet extension for browsers.

## **Installation & Setup**

### **Step 1: UNIX User Setup & Avalanche CLI Installation**

1. **Create a UNIX User:**
   - Launch Ubuntu on WSL and set up a UNIX user named `hrishikesh`.
   - Configure your environment variables and paths as needed.

2. **Install Avalanche CLI:**
   - Execute the following commands to download and install the Avalanche CLI:
     ```bash
     curl -L https://github.com/ava-labs/avalanche-cli/releases/download/v1.7.1/avalanche-cli-v1.7.1-linux.zip -o avalanche-cli.zip
     unzip avalanche-cli.zip -d avalanche-cli
     sudo mv avalanche-cli/avalanche /usr/local/bin/
     ```
   - Verify the installation by running `avalanche --version`.

### **Step 2: HrishikeshSubnet Creation**

Using the Avalanche CLI, initiate the creation of the custom blockchain subnet, HrishikeshSubnet. The following parameters are configured for this subnet:

- **VM ID:** `nzxURfeht7efcw5M8Kj8uDF4oNVqCZXqNaNvst3v2mrjfwYcr`
- **VM Version:** `v0.6.8`
- **Chain ID:** `14042`
- **Subnet ID:** `26eqgD4Kt1MvTKXC9BDjEwBAfhcBcHCKj2EXjR2UuFpSWoAHhw`
- **Blockchain ID (HEX):** `0x3d74dfa227ecec4292d8d7e171c5fdaf92e81e62e645a748d5fef1a2e6dbfd67`
- **Token Name:** `HRM Token`
- **Token Symbol:** `HRM`

**Teleporter Deployment:**

- **Messenger Contract Address:** `0x253b2784c75e510dD0fF1da844684a1aC0aa5fcf`
- **Registry Contract Address:** `0x5a313c1A34A342DE0f0833820300991Cd1c452E3`

### **Step 3: Node Configuration**

HrishikeshSubnet is decentralized, supported by multiple nodes, each with a unique ID and URL:

- **Node 1:** `NodeID-7Xhw2mDxuDS44j42TCB6U5579esbSt3Lg` – `http://127.0.0.1:9650`
- **Node 2:** `NodeID-MFrZFVCXPv5iCn6M9K6XduxGTYp891xXZ` – `http://127.0.0.1:9652`
- **Node 3:** `NodeID-NFBbbJ4qCmNaCzeW7sxErhvWqvEQMnYcN` – `http://127.0.0.1:9654`
- **Node 4:** `NodeID-GWPcbFJZFfZreETSoWjPimr846mXEKCtu` – `http://127.0.0.1:9656`
- **Node 5:** `NodeID-P7oB2McjBGgW2NXXWVYjV8JEDFoW9xDE5` – `http://127.0.0.1:9658`

### **Step 4: MetaMask Integration**

To interact with HrishikeshSubnet via MetaMask:

1. **Network Configuration:**
   - Open MetaMask and navigate to **Settings** > **Networks** > **Add a Network**.
   - Input the following parameters:
     - **Network RPC URL:** `http://127.0.0.1:9650/ext/bc/hrishikeshSubnet/rpc`
     - **Network Name:** `hrishikeshSubnet`
     - **Chain ID:** `14042`
     - **Token Symbol:** `HRM`
     - **Token Name:** `HRM Token`

2. **Verification:**
   - Ensure that the connection is successful by checking the network status in MetaMask.

## **Smart Contract Deployment**

The Solidity smart contract in this repository implements a standard ERC20 token with additional minting and burning capabilities.

### **Mint Function**

```solidity
function mint(address to, uint256 amount) public onlyOwner {
    _mint(to, amount);
}
```

- **Functionality:** Creates new tokens and assigns them to the specified address.
- **Access Control:** Restricted to the contract owner, ensuring that token creation is regulated.

### **Burn Function**

```solidity
function burn(uint256 amount) public {
    _burn(msg.sender, amount);
}
```

- **Functionality:** Allows token holders to burn (destroy) their tokens, reducing the total supply.
- **Access Control:** The burn action is limited to the caller's tokens, preventing unauthorized token destruction.

## **Technical Considerations**

- **Security:** The smart contract is developed following best practices, including the use of access modifiers to control sensitive functions like minting.
- **Scalability:** The decentralized nature of HrishikeshSubnet, supported by multiple nodes, ensures that the network can scale efficiently.
- **Compatibility:** The network configuration is designed to work seamlessly with MetaMask, providing a user-friendly interface for interacting with the blockchain.

## **Conclusion**

The HrishikeshSubnet project offers a robust foundation for developing, deploying, and testing decentralized applications in a private, controlled blockchain environment. By integrating with MetaMask, this setup provides a practical, real-world-like testing ground for developers. The included ERC20 token contract further enhances the ecosystem by offering controlled token minting and burning capabilities.

## **Acknowledgments**

This project draws upon the latest advancements in blockchain technology, with special thanks to the Avalanche team for their continued innovation and support. Acknowledgment is also extended to the open-source community for their contributions to blockchain and smart contract development.

## **License**

This project is licensed under the MIT License—see the [LICENSE](LICENSE) file for details.
**Necessary Screenshot of task done in ubuntu **

![block1](https://github.com/user-attachments/assets/0c985b2f-dc02-4c64-87c3-afe245809fe2)

![block2](https://github.com/user-attachments/assets/1af20f8b-2385-43a8-8f92-d44162b6c499)

![block3](https://github.com/user-attachments/assets/b0b1e8de-33a9-40f1-a318-75d92ee556c3)

![block4](https://github.com/user-attachments/assets/ca65eee2-285c-4e32-8c61-6aa5792873dc)

![block5](https://github.com/user-attachments/assets/1fd5e233-ecb3-4dd6-9120-3157e99b6e3c)

Metamask integration with local host

![block6](https://github.com/user-attachments/assets/d9cfd7a6-aab6-4dac-8140-85e2a0dbb860)

---

