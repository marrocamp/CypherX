Syntax: `/register <password> [email]`  
Permission Node: `xauth.register` (Only used when forced registration is disabled to specify which groups/players should register)  
Description: Registers the current player with the defined password and email (if given)

Syntax: `(/login|/l) <password>`  
Description: Allows a player to access their account  

Syntax: `(/changepw|/changepass|/cpw|/changepassword) <old password> <new password>`  
Description: Allows a player to change their password

Syntax: `/logout`  
Description: Ends the current players session

**(All commands below this point, except `/xauth location`, can be used in the server console)**

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

Syntax: `/xauth (config|conf) <setting> [value]`  
Permission Node: `xauth.admin.config`  
Description: View information about or change a xAuth setting

Syntax: `/xauth reload`  
Permission Node: `xauth.admin.reload`  
Description: Reload the xAuth configuration

Syntax: `/xauth version`  
Description: Displays the version of xAuth being used.