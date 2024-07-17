# Pump.fun Bump-Bot
A micro buy, bump bot for pumping your pump.fun tokens, the bot is free to use, however I would really appreciate if you could donate to my wallet at the bottom of the page, thank you! By using this bot your tokens will always be on the front page.

# Description
This bot automatically buys and sells on Pump.fun and Raydium.
Ideal for showcasing on the Pump.fun main page.

# Demo

[![Demo](https://img.youtube.com/vi/X5rz-T2F4qw/0.jpg)](https://www.youtube.com/watch?v=X5rz-T2F4qw)

# Download via git clone

If you have git installed on your computer you can fetch the content of this repository with the command

``` 
git clone https://github.com/EVMBotDev/pump.fun-bump_bot.git
```

# Download via ZIP

https://github.com/EVMBotDev/pump.fun-bump_bot/archive/refs/heads/main.zip

Download and extract then continue to the follow steps

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
1. RPC endpoint to connect to the Solana blockchain (Quicknode or Helius provide good free RPC endpoints).

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
If you want to adjust the buy amount in SOL, you can set it the value at the top of the script:

```
const SOL_BUY_AMOUNT =

```
Same goes for the slippage, it can be setup at the top of the script:

```
const SLIPPAGE = 
```
And the same applies for the fees (higher fees = faster speed):

```
const FEES =
```

# If you are feeling generous buy me a coffee!

SOL adress: 9morc2r3NW4krcUuh934ZuJs7MnCJxECjWdAG35oCkqN
