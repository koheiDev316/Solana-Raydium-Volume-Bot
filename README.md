# Solana-Raydium-Volume-Bot

This is a Solana trading bot designed to generate volume on the Raydium decentralized exchange. It allows users to create multiple wallets, distribute SOL and WSOL to them, and then execute bundled swaps to generate trading volume for a specific market ID.

## Features

- **Wallet Management**: Create and manage multiple keypairs to be used for trading.
- **Token Distribution**: Distribute SOL and WSOL to the generated wallets.
- **Volume Generation**: Execute bundled swaps (buy and sell) to generate trading volume on Raydium.
- **Jito Integration**: Sends transactions as bundles to Jito for potentially faster and more reliable execution.
- **Simulation**: Calculate potential volume and SOL loss before executing real trades.

## Prerequisites

- Node.js and npm installed.
- A Solana wallet with some SOL to pay for transaction fees and to fund the trading wallets.

## Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/koheiDev316/Solana-Raydium-Volume-Bot-main.git
    cd Solana-Raydium-Volume-Bot-main
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Configure the bot:**
    Open `config.ts` and fill in the following values:
    - `connection`: Your RPC URL.
    - `wallet`: The secret key of your main wallet that will be used to send SOL and WSOL to the trading wallets.

## Usage

The main entry point of the application is `main.ts`. You can run the bot with the following command:

```bash
npm start
```

This will present you with a menu of options:

1.  **Create Keypairs**: This option allows you to create new wallets or use existing ones. The keypairs will be stored in the `src/keypairs` directory.
2.  **Distribute SOL/WSOL**: This option allows you to send SOL and WSOL to your created wallets.
3.  **Simulate Volume**: This option calculates the potential volume and SOL loss based on your inputs, without executing any real trades.
4.  **Start Volume**: This option starts the volume generation process. You will be prompted to enter the market ID, the number of swaps to perform, the delay between swaps, and the Jito tip amount.
5.  **Reclaim SOL/WSOL**: This option allows you to send all the SOL and WSOL from your trading wallets back to your main wallet.

### Example Workflow

1.  Run the bot and select option `1` to create new keypairs.
2.  Select option `2` to distribute SOL and WSOL to the newly created keypairs.
3.  Select option `4` to start generating volume. Provide the market ID and other requested information.
4.  Once you are done, you can use option `5` to reclaim the remaining funds from the trading wallets.

## Disclaimer

This bot is for educational purposes only. Use it at your own risk. The author is not responsible for any financial losses.

