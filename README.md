---
description: Official documentation about Discord Bot Builder.
---

# Get Started

At the Moment we only Support and Document the Beta because this is the all new DBB!

## 1.Get the Beta

Go to you Steam Libary and open the "Propertis" of DBB and Activate the beta \(Pictures\).

Make shure DBB is closed. If not you cant change the Version to Beta.

![Picture Steam Lib](.gitbook/assets/steam-lib.png) ![Picture Game Settings](.gitbook/assets/steam-beta.png)

## 2. Make a Project

Wait until the download of the Beta is done \(if you have to\) and start DBB create a new or open a Project.

```text
The Bot Folder name is the Name of the Folder that gets Created.
The Bot Folder Path is the path to the Bot.

Exaple:
    Bot Folder Name : MyFirstBot
    Bot Folder Path : C:/User/Desktop
    This means the Bot is saved on the Desktop in the Folder MyFirstBot.
```

## 3. Create a Bot Account for Discord and Setup up in DBB

Login on to the [Discord Developer Dashboard](https://discordapp.com/developers/applications/) and create a new Appilication give it a Name. Select your new App and click on "Bot", create a Bot User for this App with "Add Bot". Change the Settings of your Bot like you want. _\(the Permissons tab is not a setting, you don't need this here.\)_ After this copy your Token by clicking on "copy". **BE VERY CAREFUL WITH THIS TOKEN, ANYONE CAN ABUSE YOUR BOT AND THE SERVERS FROM IT**

Go to DBB and Open your Projet for this Bot. Click on Bot in the Menubar and "Set Bot Token" and paste the Token from the Discord Devsite there. _You can use the Hotkey too \(ctrl + alt + t\)_

**Currently Broken** After this use "Generate Bot Invite" in the "Bot" Menu to add the Bot to your Server. _more comming soon_

**Default Way** Go back to your Appilication on the Discord Developer Dashboard and click on "OAuth2". And Select by Scopes "bot". A new Menu show up below and you can select what Permissons the Bot need to work right. This creates a Own role on the Server for the Bot. If you want to manage the role by yourself / the Users set no Permissons and no Role will be Created.

![Picture Discord Dashboard](.gitbook/assets/discord-devboard-oauth.png)

If no Permissons are set for the Bot he has the "@everyone" Permissons or you can give it a "Role" with permissons selected by yourself.

Copy the Link and Open it in the Browser of your Choice. If you get a Login Prompt from Discord login and open the Link again if you get Rediricted after login to Discord Web insted of the Bot Invite. Select the Server to Invite and the Permissions that you want to be set if any. Press autorize and solve the Re-Captcha. Now the Bot is ready to work on your Server. If you want to invite the Bot to other Server simply share the Link or use it again. _\(Make sure the Bot is Public that other People can add it via the Link\)_

## 4. Create a Command

To create a Command click on the green "plus" Button and select the new Command. Click on Open to get on the Workspace.

### 4.1 Add Blocks

If you Rightclick on any free spot you get the Menu to add [Blocks](faq/blocks.md) to your Workspace.

In the Tab "Events" we have some Blocks when the Bot starts to execute a Command/Action. In our Case we use the "Message Sent \[EVENT\]" to to start whenever the bot resives a Message \(permissons to read on the Channel/DM\).

![Picture DBB EVENTS](.gitbook/assets/dbb-events.png)

If you click on "Message Sent \[EVENT\]" a new Block apperes.

![Picture DBB Block](.gitbook/assets/dbb-hover-desc.png)

This is the beginning of your Command. Without an Event your Command never Starts working because these are the only Blocks that have no **Input** Action Connection because they get Triggerd by the Bot itself. The Event "Message Sent" gives you a Action Output and a Message Output connection. If you Hover on the Points you get a short Discription about what it is and what Type of connection it is.

### 4.2 Connect Blocks / Lines

**Lines** are the Connection of your Blocks to pass Variables and the flow of your Command \(what Block gets executed next\).

There are Different Variable types: `unspecified, undefined, null, object, boolean, number, text, list, date, action`

The type of the Line **needs to match** for connecting tow Blocks. On the Output Side there can be as many Connections per Point \(exept by the action type\) as you need / want. Input can always only be one Connection per Point.

### 4.3 Important "nice to know"

```text
Server = Guild
User != Member || Member are users that stays in dependency to the Guild. Means that you can get and set Roles and so on.
```

## Now its your Turn.

This are some Important Information about the Basics of DBB. Now you can start Building your own Flows and create awesome Commands and automated procedures.

