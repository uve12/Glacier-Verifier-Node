# Glacier-Verifier-Node
Glacier Incentivized testnet node guide

Glacier is the first data-centric blockchain to supercharge AI & DePIN at scale. Integrated with BNBCHAIN, Filecoin, ArweaveEco, Celestia, babylon Chain

Docs : [Glacier Docs](https://docs.glacier.io/) | X : [x.com](https://x.com/Glacier_Labs)


# Join the Crypto Console Community

Engage with our community across various platforms:

- **Telegram**: Join the discussion at [Crypto Console Telegram](https://t.me/cryptoconsol)
- **X (Twitter)**: Follow our updates on [Crypto Console X](https://www.x.com/cryptoconsol)
- **YouTube**: Subscribe for videos at [Crypto Console YouTube](https://www.youtube.com/@cryptoconsole)

---

# VPS Options

If you're looking for a Virtual Private Server (VPS) to host your crypto projects, here are some options using various payment methods like Credit Card, PayPal, or Crypto Credit Card:

- **VPS 1**: [Contabo: Cloud VPS 1](https://www.jdoqocy.com/click-101278318-15692486)
- **VPS 2**: [Contabo: Cloud VPS 2](https://www.tkqlhce.com/click-101278318-13796472)
- **VPS 3**: [Contabo: Cloud VPS 3](https://www.dpbolvw.net/click-101278318-13796474)
- **VPS 4**: [Contabo: Cloud VPS 4](https://www.anrdoezrs.net/click-101278318-13796476)

---

## Hardware Requirements

Below are the minimum hardware specifications needed to run our services efficiently:

| **Component** | **Minimum Requirement** |
|---------------|-------------------------|
| **CPU**       | 2 Cores                 |
| **RAM**       | 4 GB                    | 
| **Network**   | 8 MBps                  |

---

# Running a Glacier Verifier Node on OpBNB Testnet

## Step 1: Create New Wallet

1. **Create a New Wallet**: Use your preferred wallet solution (like MetaMask, Trust Wallet, etc.) to create a new wallet.

## Step 2: Obtain Testnet BNB

2. **Get Testnet BNB (tBNB)**:
   - Visit a faucet for the BNB Smart Chain (BSC) Testnet, like the [official BNB Testnet Faucet](https://testnet.binance.org/faucet-smart).
   - Request some tBNB to your new wallet address.

## Step 3: Bridge tBNB to OpBNB Testnet

3. **Bridge tBNB**:
   - Go to the [BNB Chain Bridge](https://testnet.bnbchain.org/en/bridge) or https://opbnb-testnet-bridge.bnbchain.org/deposit .
   - Transfer the tBNB from the BNB Testnet to the OpBNB Testnet.

## Step 4: Prepare Your Node's Private Key

4. **Copy Private Key**:
   - From your wallet, copy the private key of your node wallet. **Do not include the `0x` prefix**.

## Step 5: Deploy the Verifier Node

5. **Run the Node**:

   - Join : [glacier.io](https://www.glacier.io/points/?inviter=0x8D2413447FF297d30BdC475F6D5cb00254685aae)

   - Ensure you have Docker installed on your machine.
     ```bash
      sudo apt update & sudo apt upgrade -y
      sudo apt install ca-certificates zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev curl git wget make jq build-essential pkg-config lsb-release libssl-dev libreadline-dev libffi-dev gcc screen unzip lz4 -y
      curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
      echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
      sudo apt-get update
      sudo apt-get install docker-ce docker-ce-cli containerd.io
      docker version
     ```
   - Use the following command to start your verifier node:

     ```bash
     docker run -d -e PRIVATE_KEY=$YOUR_PRIVATE_KEY --name glacier-verifier docker.io/glaciernetwork/glacier-verifier:v0.0.2
     ```

   - Replace `$YOUR_PRIVATE_KEY` with the private key you copied (without `0x`).

    Ex: **docker run -d -e PRIVATE_KEY=99b2a8983b93c9328d938 --name glacier-verifier docker.io/glaciernetwork/glacier-verifier:v0.0.1**

6. **Ensure Faucet Useage**:
   - Before running the node, make sure you've obtained tBNB from the faucet.

## Step 6: Monitor Your Node

7. **Check Logs**:
   - To view the logs of your node for debugging or monitoring:

     ```bash
     docker logs -f glacier-verifier
     ```

8. **Check Node Status**:
   - You can check the online status of your verifier node on the testnet at:
     - **[Glacier Testnet Node Status](https://testnet.nodes.glacier.io/status)**


Follow : https://x.com/cryptoconsol
