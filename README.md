---
description: This is the official documentation of Discord Bot Builder with the collaboration of the community.
---
## What is Discord Bot Builder?
Discord Bot Builder is a piece of software with which you can develop your own Discord bot using a GUI. You can buy it on Steam [here](https://store.steampowered.com/app/1119570/Discord_Bot_Builder/).

## What is our Discord server?
We offer to the community the opportunity of ask of support and meet new people in our [Discord server](https://discord.gg/PAzxTDw)

# Get Started

We will only support and document the beta version of DBB because this is the rewritten version.

## 1. Get the Beta Version

Open Steam and go to your library.
Right click on Discord Bot Builder and select Properties.
<br>![Right Click Menu](https://heroku.is-a-bad.host/i/qvwi.png)<br>
In the new window that came up, select the Betas tab at the top then in the dropdown menu, select the beta version. If you can't open the dropdown menu, make sure DBB is closed.
<br>![Selecting Beta](https://heroku.is-a-bad.host/i/47eh.png)<br>

## 2. Create Your First Project

If you need to, wait until the beta version has downloaded and start DBB. You will be greeted with this screen:
<br>![Main Screen](https://heroku.is-a-bad.host/i/6cyb.png)<br>
Click on Create New Project. You should now have this screen:
<br>![Create New Project Screen](https://heroku.is-a-bad.host/i/j0aw.png)<br>
The Bot Folder Name is the name of your project and the name of the folder that will contain your bot.
The Bot Folder Path is the directory on your computer where the new folder containing your bot will be created.
For example:
<br>![Create New Project Example](https://heroku.is-a-bad.host/i/7b7i.png)<br>
The bot will be saved on my desktop in the folder and with the project name 'My First Bot'.

## 3. Create a New Bot Account and Set it Up in DBB

Go on to the [Discord Developer Portal](https://discordapp.com/developers). If you've never made a bot before, you should be shown this screen:
<br>![Empty Developer Portal](https://heroku.is-a-bad.host/i/njjm.png)<br>
Create a new application and give it a name.
<br>![Creating New Application](https://heroku.is-a-bad.host/i/0k7v.png)<br>
When you've clicked Create App, this should come up:
<br>![Bot General Info](https://heroku.is-a-bad.host/i/z2u6.png)<br>
Go to Bot on the side, and create the bot:
<br>![Creating Bot](https://heroku.is-a-bad.host/i/w9rx.png)<br>
You should now have this screen:
<br>![Bot Info](https://heroku.is-a-bad.host/i/h8mz.png)<br>
If you want to make it so only you can invite the bot \(e.g. if it's a custom bot for your server\), just click the slider under Public Bot:
<br>![Public Bot Slider](https://heroku.is-a-bad.host/i/a55q.png)<br>
Copy your bot's token. **MAKE SURE TO KEEP THE TOKEN SECRET AT ALL TIMES! IF SOMEBODY GETS THE BOT TOKEN, CAN ACCESS AND ABUSE YOUR BOT!** I am showing my token for documentation reasons, you should *never* show yours.
<br>![Copying Token](https://heroku.is-a-bad.host/i/mcf1.png)<br>
Input it into DBB. Do this by selecting the Bot menu in the toolbar at the top of the screen and selecting Set Bot Token. \(you could also do the keyboard shortcut **Ctrl** + **Alt** + **T**.\) Then paste the token and hit Enter or click OK.
<br>![Setting Token](https://heroku.is-a-bad.host/i/esq5.png)<br>
Now you need to invite the bot to your server. Get an invite link by going to the Bot menu in the toolbar at the top of the screen and selecting Generate Invite. \(you could also do the keyboard shortcut **Ctrl** + **G**.\)
<br>![Getting Invite Link](https://heroku.is-a-bad.host/i/rvwr.png)<br>
Then go to your web browser and paste the invite link there. Choose which server you want to invite the bot to and click Continue.
<br>![Inviting the Bot I](https://heroku.is-a-bad.host/i/31l6.png)<br>
On the next page, a huge list of permissions will come up. Change them as you wish. Scroll down to the bottom \(there will be some information about your bot\) and click Authorize.
<br>![Inviting the Bot II](https://heroku.is-a-bad.host/i/fjii.png)<br>
Finally, complete the reCAPTCHA, click Verify, and this message should display:
<br>![Successfully invited the bot](https://heroku.is-a-bad.host/i/fgcr.png)<br>
That means you're all set and the bot's now in your server.
<br>![Bot Profile](https://heroku.is-a-bad.host/i/ww5x.png)<br>

## 4. Create a Command

To create a new command, click on the green + button next to the search bar at the top of the screen.
<br>![Green Plus](https://heroku.is-a-bad.host/i/4d54.png)<br>

### 4.1. Customising Your Workspace

Once you have clicked on the + icon, a new workspace was created.
<br>![New Workspace](https://heroku.is-a-bad.host/i/y4in.png)<br>
You can customise the thumbnail, title and description.

#### 4.1.1. Customising the Thumbnail

To customise the thumbnail of a workspace, hover over the empty grey space on the top right of the screen. Click on it, paste an image and hit enter or click OK. Boom! You're done.
<br>![Customising Thumbnail](https://heroku.is-a-bad.host/i/8une.png)<br>
Now your workspace looks nice and pretty.
<br>![Nice and Pretty](https://heroku.is-a-bad.host/i/nobz.png)<br>

#### 4.1.2. Customising the Title

To customise the title of a workspace, click on My New Workspace and change it. Simple as.
<br>![Customising Title](https://heroku.is-a-bad.host/i/j55a.png)<br>

#### 4.1.3. Customising the Description

To customise the description of a workspace, click anywhere on the empty space above the 3 buttons at the bottom. Then type whatever you want. Simple as.
<br>![Customising Description](https://heroku.is-a-bad.host/i/utk1.png)<br>

### 4.2. Adding Blocks

If you right-click on any empty spot in the workspace, the Blocks menu comes up. In the Events tab, there are some blocks so the bot can execute an action. In these docs, I will use the Message Sent Event block to execute an action whenever the bot receives a message \(either in the server or its DMs\).
<br>![Adding a Block](https://heroku.is-a-bad.host/i/b9gb.png)<br>
This is the beginning of your command. The Message Sent Event block has an Action Output and a Message Output. If you don't know what this means, DBB is also well documented: whenever you hover over anything, it tells you what it is:
<br>![Message Sent Event Block Description](https://heroku.is-a-bad.host/i/1duq.png)<br>

## 4.3. Good to know

Server = Guild
User ≠ Member \(a member is a user that is relevant to the guild only. you can execute actions to do with a specific server with a member\)

### 4.4. Your Turn

Use these docs and the example workspace provided to you to make your own bot!


# Contributors

ACertainCoder#9011<br>
Ju#2402<br>
monksharru#6969<br>
MrGold#0001
