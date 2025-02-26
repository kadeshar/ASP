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

Additional features:
- Trion control panel (Server launcher)
- Website (Simple website + armory + playermap)
- WoWSim (SimulationCraft alternative)
- Keria3 (Database editor)

Client addons:
- AzerothCoreAdmin
- AuctionnerSuite (working with AzerothCore)
- DBM (modern version)
- Multibot (supported playerbot control)
- Unbot (unsupported playerbot control)
- WowSimsExporter (String exporter for WoWSim)
- Transmog addons (dedicated for module)

## _**Installation**_

- install dependencies from folder Installations. \
IMPORTANT: Script xampp.bat must be run always when ASP change location
- restart computer
- download WoW 3.3.5 client\
	Classic: https://www.chromiecraft.com/en/downloads/ \
	Modern (Zavarius): https://1fichier.com/?0qauls7p3cl83dplz2je
- change file located in WoW client Data/enUS/realmlist.wtf on "set realmlist 127.0.0.1"
- to start server run file Start.bat. After launcher startup click buttons in order Database, World, Logon
- run game (default account admin/123456 which have GM)
- to start website click button "Website" in launcher. Website is available on address "localhost" 
- to stop server click buttons in order  Logon, World, Database\
IMPORTANT: Never close server by closing all windows. It can corrupt your database!!!

## _**Upgrade**_
WARNING:
- custom db modification can break update script!!!
- configs will be overridden because often structure changes!!! 

IMPORTANT: backup whole server before update

- Replace all files
- Run script "Install xampp" from Installation folder
- Reapply custom settings (especial progression)

## _**Known issues**_
- playerbots dont work in Strand of the Ancients (issue: https://github.com/liyunfan1223/mod-playerbots/issues/559)
- playerbots dont work in Isle of Conquest
- playerbots dont queue on Wintergrasp

## _**FAQ**_

### Transfer character from other repack
Instruction is in Extensions/Pdump converter. Not all repacks are supported.

### Change realm IP
Use launcher database editor and change "Address" (not "Local Address") and save. Change realmlist.wtf content in WoW client.

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
Talk with The Lich King a use option "I wish to skip the Death Knight starter questline"
