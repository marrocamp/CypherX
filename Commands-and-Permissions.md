Syntax: `/register <password> [email]`  
Permission Node: `xauth.register` (Only used when forced registration is disabled to specify which groups/players should register)  
Description: Registers the current player with the defined password and email (if given)

Syntax: `(/login|/l) <password>`  
Description: Allows a player to access their account  

Syntax: `(/changepw|/changepass|/cpw|/changepassword) <old password> <new password>`  
Description: Allows a player to change their password

Syntax: `/logout`  
Description: Ends the current players session

**(All commands below this point, excluding `/xauth location`, can be used in the server console)**

Syntax: `/xauth register <player> <password> [email]`  
Permission Node: `xauth.admin.register`  
Description: Create an account for `<player>`

Syntax: `/xauth (changepw|changepass|cpw|changepassword) <player> <new password>`  
Permission Node: `xauth.admin.changepw`  
Description: Change `<player>`'s password

Syntax: `/xauth logout <player>`  
Permission Node: `xauth.admin.logout`  
Description: End `<player>`'s session

Syntax: `/xauth unregister <player>`  
Permission Node: `xauth.admin.unregister`  
Description: Remove the account of the specified player

Syntax: `/xauth (location|loc) (set|remove) [global]`  
Permission Node: `xauth.admin.location`  
Description: Set/remove the current worlds teleport location

(Temporarily removed)  
~~Syntax: `/xauth reload`~~  
~~Permission Node: `xauth.admin.reload`~~  
~~Description: Reload the xAuth configuration~~

***

**Additional Permissions**  

`xauth.allow.player.chat` - Allow the player/group to chat while not logged in.  
`xauth.allow.player.interact` - Allow the player/group to interact with levels, switches, etc. while not logged in.  
`xauth.allow.player.move` - Allow the player/group to move while not logged in.  
`xauth.allow.player.pickup` - Allow the player/group to pick up items while not logged in.
`xauth.allow.block.place` - Allow the player/group to place blocks while not logged in.  
`xauth.allow.block.break` - Allow the player/group to break blocks while not logged in.  
`xauth.allow.entity.damage` - Allow the player/group to give and receive damage while not logged in.  
`xauth.allow.entity.target` - Allow the player/group to be targeted (followed) by mobs while not logged in.

`xauth.disallow.player.chat` - Prevent the player/group from chatting while not logged in.  
`xauth.disallow.player.interact` - Prevent the player/group from interacting with levels, switches, etc. while not logged in.  
`xauth.disallow.player.move` - Prevent the player/group from moving while not logged in.  
`xauth.disallow.player.pickup` - Prevent the player/group from picking up items while not logged in.
`xauth.disallow.block.place` - Prevent the player/group from placing blocks while not logged in.  
`xauth.disallow.block.break` - Prevent the player/group from breaking blocks while not logged in.  
`xauth.disallow.entity.damage` - Prevent the player/group from giving and receiving damage while not logged in.  
`xauth.disallow.entity.target` - Prevent the player/group from being targeted (followed) by mobs while not logged in.