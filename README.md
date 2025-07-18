# AzerothCore Single Player

Release repository for repositories https://github.com/stars/kadeshar/lists/azerothcore-single-player

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

Additional features:
- Trion control panel (Server launcher)
- Website (Simple website + armory + playermap)
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
- install dependencies from folder Installations.
- restart computer
- download WoW 3.3.5 client\
	Classic: https://www.chromiecraft.com/en/downloads/ \
	Modern (Zavarius): https://1fichier.com/?0qauls7p3cl83dplz2je
- change file located in WoW client Data/enUS/realmlist.wtf on "set realmlist 127.0.0.1"
- to start server run file Start.bat. After launcher startup click buttons in order Database, World, Logon
- run game (default account admin/123456 which have GM)
- to start website click button "Website" in launcher. Website is available on address "localhost" 
- to stop server click buttons in order  Logon, World, Database\
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

### Repack commands
Azerothcore https://www.azerothcore.org/wiki/gm-commands
Playerbots https://github.com/liyunfan1223/mod-playerbots/wiki/Playerbot-Commands

### Transfer character from other repack
Instruction is in Extensions/Pdump converter.
Supported source repacks:
- SPP wotlk (DB:18)
- Skuly wotlk
- Zaicopx wotlk
- Zavarius wotlk

### Change realm IP
Run database using launcher. Use launcher database editor and change "Address" (not "Local Address") and save. Change realmlist.wtf content in WoW client. Setup firewall to allow traffic for ports 8085 and 3724.

### Change progression
Detailed instruction is in file ASP/Extensions/Progression/Progression - instruction.txt

### Install addons
Addons are located in folder ASP/Extensions/Addons. Copy them to your WoW Client Interface folder.

### Summon transmogrifier
Use command GM command ".transmog portable"

### Synchronize transmog addon
Use in-game command ".transmog sync"

### Database credentials
Login: acore
Password: acore

### Open world PVP
Open ASP/Server/config/modules/playerbots.conf.dist file in notepad and search phrase "# PvP Enabled".
Comment and uncomment right variant (# on beginning line mean commented line) and restart world server
Open Server/config/worldserver.conf file in notepad and search phrase "GameType".
Change that value on 8 for open world pvp.

### Raids/dungeons with bots
- create other accounts using azerothcore command ".account create accountname password"
- create characters which you want in your guild (max 10 per account)
- adjust characters
	- use azerothcore command ".char level 80" to change bot level
	- use playerbot command "talents" to check current bot spec
	- use playerbot command "talents spec list" to check available for bot class specs
	- use playerbot command "talents spec specname" to switch bot to specific spec
	- use playerbot command "autogear" to gear bot for current spec
	- use playerbot command "maintenance" to learn all spell and skills, enchant gear and supplement consumables for current spec
- create guild using azerothcore command ".guild create GuildMasterCharacterName "Guild Name""
- add all bots to guild using azerothcore command "guild invite botname "Guild Name"

### Launcher is running with strange fonts and missing features
Go to ASP\Server\tools\Trion Control Panel and in TrionControlPanelDesktop.exe properties tab Compatibility set override high DPI scaling behavior on System (Enhanced).

### Skip death knight starting area
Talk with The Lich King and use option "I wish to skip the Death Knight starter questline"

### Use local LLM on bots
Instruction is located in ASP\Extensions\Ollama\Instruction.txt

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