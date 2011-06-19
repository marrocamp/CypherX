There are several commands supported by xAuth that add a range of functionality from letting a player register or log in to allowing a player with the correct permissions manage other players from in-game or through the server console.  These commands are detailed below.

***
_**Player (in-game) commands:**_

**/register \<password\>** - Registers the current player with the specified password  

**/login \<password\>** - Attempts to log the current player in  

**/changepw \<newpassword\>** - Allows an authenticated player to change their password  

**/changepw \<player\> \<newpassword\>** - Change a players password (requires correct permission level)  

**/unregister \<player\>** - Unregister a player (requires correct permission level)

**/authreload** - Reloads the configuration and account files. (requires correct permission level)  

**/toggle \<reg | changepw | autosave | filter | blankname | verifyip | strike | forcereg\>** - Toggle registration, password changes, or autosave on/off.  

**/logout** - Terminates the session of the player who uses the command.  

**/logout \<player\>** - Terminates the session of the specified player. (requires correct permission level)

***

_**Console commands:**_

**/register \<player\> \<password\>** - Registers \<player\> with the specified password  

**/changepw \<player\> \<password\>** - Changes \<player\>'s password to \<newpassword\>  

**/unregister \<player\>** - Unregister \<player\>  

**/authreload** - Reloads the xAuth configuration and account files  

**/toggle \<reg | changepw | autosave | filter | blankname | verifyip | strike | forcereg\>** - Toggle registrations, password changes, or autosave on/off.  

**/logout \<player\>** - Terminate the session of the specified player.