# Bump-Bot for Pump.fun and Raydium
This bot will buy and sell tokens automatically keeping you at the top of Pump.fun's main page OR inflate Volumes on Raydium.

# Download the bot
If you have git installed on your computer you can fetch the content of this repository with the command

``` 
git clone https://github.com/PasusS0ldev/Micro-Buy-Bot-for-Pump.Fun.git
```
Else, you can download the repository in a zip here : 
```
https://github.com/EVMBotDev/pump.fun-bump_bot/archive/refs/heads/main.zip
```

# Setting up the bot

Node.js installation is required to set up the bot:

For Windows and Mac OS follow this link: https://nodejs.org/en/download/package-manager and choose the latest version. 

For Linux, execute the following command in terminal:
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

nvm install 22
```
To check if Node.js is installed:

+ For Windows, open cmd.exe and run the command:
```
node -v
```
+ For MacOs & Linux, open terminal, and run the same command:
```
node -v
```
It should return the version of Node.js.

# Installing dependencies
In order to run the bot, you need to open cmd.exe or terminal, and navigate to the Micro Buy Bot folder with the command:

```
cd /path/to/the/folder
```
Then, in cmd.exe or terminal, run the following command:

```
npm install
```
It should install all the dependencies in a new folder named "node_modules".

# Setting up the bot

You have three things to setup within the index.js file:
1. RPC endpoint to connect to the Solana blockchain (Chainstack, Quicknode or Helius provide reliable free RPC endpoints).

2. Private key of the wallet that will execute buy and sell operations.

3. Contract address of the token you intend to bump.

The variables are on at top of the script:

```
const RPC_URL = ""; // 
const PRIVKEY = ""; // 
const TOKEN_ADDR = ""; // 
```
# Run the Bump Bot

To run the bump bot, in cmd.exe or terminal, execute the following command:

```
node index.js
```
The bot will buy the token four times and then sell all the balance.

# Adjustments

If you want to adjust the number of times to buy before selling, you can find it at the bottom of the script.

```
// Buy
promises.push(swap(SOL_ADDR, TOKEN_ADDR, solanaTracker, keypair, connexion, SOL_BUY_AMOUNT));
promises.push(swap(SOL_ADDR, TOKEN_ADDR, solanaTracker, keypair, connexion, SOL_BUY_AMOUNT));
promises.push(swap(SOL_ADDR, TOKEN_ADDR, solanaTracker, keypair, connexion, SOL_BUY_AMOUNT));
promises.push(swap(SOL_ADDR, TOKEN_ADDR, solanaTracker, keypair, connexion, SOL_BUY_AMOUNT));
```
If you want to buy only 2 times, for example, you just need to remove 2 lines, like this:

```
// Buy
promises.push(swap(SOL_ADDR, TOKEN_ADDR, solanaTracker, keypair, connexion, SOL_BUY_AMOUNT));
promises.push(swap(SOL_ADDR, TOKEN_ADDR, solanaTracker, keypair, connexion, SOL_BUY_AMOUNT));
```
# Adjusting the buy amount, slippage and fees


EVMBotDev has implemented a buy range, so you can set the minimum and maximum amount to buy where the bot will randomly choose an amount between the two values:

```
const MIN_SOL_BUY_AMOUNT = ""; //
const MAX_SOL_BUY_AMOUNT = ""; //

```
Same goes for the slippage, it can be setup at the top of the script:

```
const SLIPPAGE = 
```
And the same applies for the fees (higher fees = faster speed):

```
const FEES =
```
Happy bumping!

# If you are feeling generous buy me a coffee!

SOL adress: 9morc2r3NW4krcUuh934ZuJs7MnCJxECjWdAG35oCkqN
