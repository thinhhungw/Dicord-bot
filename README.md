## 🚀 HOW TO MAKE A DISCORD BOT  
## 📌 STEP 1: Install `Node.js`  
- JavaScript requires Node.js to run outside a browser, and Discord bots also use `Node.js`.  
### 🔍 1. Check if you already have Node.js installed  
- Open Command Prompt (cmd) or PowerShell (`Windows + R`, type `cmd`, then press Enter).  
- Run the following command: ```node -v```
- If it shows a version number (e.g., v18.16.0), Node.js is installed, and you can skip Step 2.  
- If you see "node is not recognized," you need to install Node.js.  
## 📌 STEP 2: Install Node.js  
### 🔽 1. Download `Node.js`  
- Go to the official website: `https://nodejs.org/`  
- Download the LTS (Long Term Support) version (it's more stable).  
- Run the installer and click "Next" until the installation completes. 
### ✅ 2. Verify the installation  
- Open cmd again and run: ```node -v```
- - If it displays a version number, the installation was successful.  
### 🎯 Node.js comes with npm (Node Package Manager). Check by running: ```npm -v```
### 📂 Add Node.js to PATH (if needed)  
- Press `Windows + S`, search for `Edit the system environment variables`, and open it.  
- Go to the **Advanced** tab → Click **Environment Variables**.
- In **System variables**, find **Path**, and click **Edit**.  
- Click **New**, then add these paths (adjust based on your installation location):  
```
C:\Program Files\nodejs\
C:\Users\<Your-Username>\AppData\Roaming\npm\
```
- Replace `<Your-Username>` with your Windows account name.  
## 📌 STEP 3: Install VS Code and Open Your Project  
### 🔽 1. If you don’t have VS Code  
- Download from `https://code.visualstudio.com/` 
- Install it normally (just keep clicking Next).
### 📂 2. Open VS Code and Create a Bot Folder  
- Open VS Code.  
- Create a new folder on your Desktop (or anywhere), name it **"discord-bot"**.  
- In VS Code, go to **File → Open Folder…**, and select your **discord-bot** folder. 
## 📌 STEP 4: Initialize a Node.js Project  
- In VS Code, open the terminal (`Ctrl + J`).  
- Run the following command: ```npm init -y```
- This will generate a **package.json** file containing project details.  
## 📌 STEP 5: Install the `discord.js` Library  
- - In the terminal, run: ```npm install discord.js```
- This command will download the `discord.js` library, which allows the bot to interact with Discord.  
## 📌 STEP 6: Create the Bot File  
- Inside the **discord-bot** folder, create a new file named **`index.js`**.  
- Create a new file named `index.js`.
- Open the file `index.js`, paste the following code into it:
```
const { Client, GatewayIntentBits } = require('discord.js');
const client = new Client({ intents: [GatewayIntentBits.Guilds] });

client.once('ready', () => {
    console.log(`Bot is online!`);
});

client.login('YOUR_BOT_TOKEN');
```
### Lưu ý:
- Replace 'YOUR_BOT_TOKEN' with your actual Discord bot token.
- If you don’t have a token yet, proceed to the next step.
## 📌 STEP 7: Create a Discord Bot and Get a Token
### 🔽 1. Go to Discord Developer Portal
- - Open: `https://discord.com/developers/applications`
- Click New Application, enter a name, and create it.
- Navigate to the Bot tab, click Add Bot, then select `Yes, do it!`
- Scroll down and enable `Message Content Intent` (if you want the bot to read messages).
- Click Reset Token → Copy the token (keep it safe, you'll need it in `index.js`).
### 🔽 2. Add the Bot to Your Discord Server
- Go to OAuth2 → URL Generator.
- Under Scopes, select bot.
- Under Bot Permissions, choose the necessary permissions (e.g., Administrator).
- Scroll down, copy the generated link, paste it into your browser, and add the bot to your server.
## 📌 STEP 8: Run the Bot
- Go back to VS Code and open the terminal.
- Run the following command: ```node index.js```
- If you see "Bot is online!", the bot is running successfully! 🎉
## 📌 STEP 9: Test the Bot on Discord
- Open Discord and check if your bot is online in the server.
- If it's online, congratulations! Your bot is now running. 🎊
