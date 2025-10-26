# AzerothCore Single Player

<strong>AzerothCore Single Player</strong> is a curated collection of modules and add-ons for AzerothCore, designed to provide a comprehensive single-player World of Warcraft testing environment. The entire experience is packaged into an easy-to-install and ready-to-launch package.

This custom build features:

- <strong>Playerbots:</strong> Advanced bots that simulate a living, breathing world around you. Powered by modern AI, they create realistic interactions, mimicking the experience of playing with real people.

- <strong>Progressive Expansion Content:</strong> Journey through the first three iconic eras of World of Warcraft: Classic (Vanilla), The Burning Crusade (TBC), and Wrath of the Lich King (WOTLK).

- <strong>Dynamic Auction House:</strong> A fully functional Auction House bot that supports the progressive expansion system, ensuring a balanced and evolving economy.

- <strong>Hardcore Mode:</strong> An optional module for players seeking the ultimate challenge and the most demanding gameplay experience.

- <strong>Quality of Life (QoL) Improvements:</strong> Various other modules designed to enhance and streamline your journey through Azeroth.

- <strong>Integrated Website:</strong> A companion website for tracking in-game statistics and progress.

Included Repositories: https://github.com/stars/kadeshar/lists/azerothcore-single-player

## _**Informations**_

Additional modules:
- Playerbots
- Playerbots level brackets
- Auctionator
- Transmog
- Progression
- Hardcore
- Skip DK starting area
- Acore mall
- Eluna
- Ollama
- Junk to gold
- Dead means dead
- PvP Titles

Additional features:
- Trion control panel (Server launcher)
- Website (Simple website + armory + playermap + pvp stats)
- WoWSim (SimulationCraft alternative)
- Keria3 (Database editor)
- Windows Memory Cleaner (Memory cleaner for long running servers)

Client addons:
- AzerothCoreAdmin
- AuctionnerSuite (working with AzerothCore)
- DBM (modern version)
- Multibot (supported playerbot control)
- Unbot (unsupported playerbot control)
- WowSimsExporter (String exporter for WoWSim)
- Transmog addons (dedicated for module)

## _**Installation**_

- put file ending with .001 and .002 in same folder and unpack .001 using [7zip](https://www.7-zip.org/). If you dont get any error that means both files are unpacked.
- install dependencies from the ASP/Installations folder.
- restart computer
- download WoW 3.3.5 client\
	Classic: https://www.chromiecraft.com/en/downloads/ \
	Modern (WotLK 3.3.5a HD Client) https://discord.gg/Gyb9Z252vt \
	Modern (Zavarius): https://1fichier.com/?0qauls7p3cl83dplz2je
- change file located in WoW client Data/enUS/realmlist.wtf on "set realmlist 127.0.0.1". In some clients this file is readonly and you have to uncheck that property in file properties.
- to start server run file Start.bat. After launcher startup click buttons in order Database, World, Logon
- run game (default account admin/123456 which have GM)
- to start website click button "Website" in launcher. Website is available on address "localhost" 
- to stop server click buttons in order  Logon, World, Database\
\
IMPORTANT: \
Never close server by closing all windows. It can corrupt your database!!!\
Remember to periodically back up the repack. Every power outage can corrupt you database!!!\
Script "ASP\Installations\Install xampp.bat" must be run always when ASP change location on disc\
Keep ASP files on SSD disc for better performance

## _**Update**_
WARNING:
- custom db modification can break update scripts!!!
- configs will be overridden because often structure changes!!! 

IMPORTANT: backup whole server before update

- put file ending with .001 and .002 in same folder and unpack .001 using [7zip](https://www.7-zip.org/). If you dont get any error that means both files are unpacked.
- From old repack folder copy ASP/Server/mysql and paste into unpacked update_only archives (same location)
- Run script "Install xampp" from Installation folder
- Reapply custom settings (especial progression)

## _**Support**_

|     |     |
|:---:|:---:|
|If you need support         |  [![](https://dcbadge.limes.pink/api/server/single-player-project-291115666097045506)](https://discord.gg/single-player-project-291115666097045506) <br> channel spp-wotlk-335 |
|If you want to support me   |  <a href="https://buymeacoffee.com/kadeshar" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a> |

## _**Known issues**_
- playerbots dont work in Strand of the Ancients (issue: https://github.com/liyunfan1223/mod-playerbots/issues/559)
- playerbots dont queue on Wintergrasp

## _**FAQ**_

### Create new account
Run command in the worldserver Windows
```account create $account $password```

### Repack commands
Azerothcore https://www.azerothcore.org/wiki/gm-commands \
Playerbots https://github.com/liyunfan1223/mod-playerbots/wiki/Playerbot-Commands

### Transfer character from other repack
Instruction is in Extensions/Pdump converter.
Supported source repacks:
- SPP wotlk (DB:18)
- Skuly wotlk
- Zaicopx wotlk
- Zavarius wotlk
- most probably other AzerothCore based repacks

### Change realm IP
Run database using launcher. Use launcher database editor and change "Address" (not "Local Address") and save. Change IP (on the same provided in launcher) in realmlist.wtf file located in your WoW client/Data/enUS (or other client language). In some clients this file is readonly and you have to uncheck that property in file properties. Setup firewall to allow traffic for ports 8085 and 3724 (and router if you want use public ip address)

### Change progression
Detailed instruction is in file ASP/Extensions/Progression/Progression - instruction.txt

### Install addons
Addons are located in folder ASP/Extensions/Addons. Copy them to your WoW Client Interface folder.

### Summon transmogrifier
Use command GM command ```.transmog portable```

### Synchronize transmog addon
Use in-game command ```.transmog sync```

### Database credentials
Login: acore\
Password: acore

### Open world PVP
Open ASP/Server/config/modules/playerbots.conf.dist file in notepad and search phrase "# PvP Enabled".
Comment and uncomment right variant (# on beginning line mean commented line) and restart world server
Open Server/config/worldserver.conf file in notepad and search phrase "GameType".
Change that value on 8 for open world pvp.

### Raids/dungeons with bots
- create other accounts using azerothcore command ```.account create accountname password```
- create characters which you want in your guild (max 10 per account)
- adjust characters
	- use azerothcore command ```.char level 80``` to change bot level
	- use playerbot command ```talents``` to check current bot spec
	- use playerbot command ```talents spec list``` to check available for bot class specs
	- use playerbot command ```talents spec specname``` to switch bot to specific spec
	- use playerbot command ```autogear``` to gear bot for current spec
	- use playerbot command ```maintenance``` to learn all spell and skills, enchant gear and supplement consumables for current spec
- create guild using azerothcore command ```.guild create GuildMasterCharacterName "Guild Name"```
- add all bots to guild using azerothcore command ```guild invite botname "Guild Name"```

### Launcher is running with strange fonts and missing features
Close launcher and go to ASP\Server\tools\Trion Control Panel and in TrionControlPanelDesktop.exe properties tab Compatibility set override high DPI scaling behavior on System (Enhanced).

### Skip death knight starting area
Talk with The Lich King and use option "I wish to skip the Death Knight starter questline"

### Use local LLM on bots
Instruction is located in ASP\Extensions\Ollama\Instruction.txt

### How to move Multibot addon
Using right mouse buttom drag and drop method on cogs icon

### How to change prices on Auction House
There is few ways to do that:
- globally you can modify in ASP/Server/configs/modules/mod_auctionator.conf.dist values Auctionator.Multipliers.Seller
- for specific item you can modify/add record in SQL table acore_characters.mod_auctionator_market_price

## _**Credits**_

Special thanks to the people without whom this project would be impossible:
- AzerothCore stuff for his huge support for core and modules https://github.com/azerothcore/azerothcore-wotlk/graphs/contributors
- Liyunfan1223 and his team making AzerothCore Playerbots https://github.com/liyunfan1223/mod-playerbots/graphs/contributors
- Celguar and his team making Cmangos Playerbots which learn me a lot about playerbots https://github.com/cmangos/playerbots/graphs/contributors
- FlyingPhoenix for his fantastic launcher https://github.com/fIyingPhoenix
- DustinHendrickson for his fantastic modules https://github.com/DustinHendrickson
- Noisiver for his fantastic modules https://github.com/noisiver
- Macx-Lio for his fantastic addon to control playerbots https://github.com/Macx-Lio
- and other which works to make WoW Emulator World alive :)