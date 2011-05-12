xAuth has many configurable settings that let you, the server manager, have nearly complete control over how it operates.  To begin configuring, first navigate to the /plugins/xAuth/ directory and open config.yml in a text editor of your choice.  

The configuration is divided up into nodes that each have one or multiple properties for easier management.  A description of these nodes and properties is below.

***
* **session:**
    * `verifyip: true`  
Enable/disable IP verification upon resuming a session.
    * `timeout: 3600`  
The length of time, in seconds, that a players session will be preserved.  During this time they will not have to re-authenticate themselves if they log out and back in.

* **notify:**
    * `limit: 5`  
The length of time, in seconds, between notification messages of an illegal action are sent to a player.

* **login:**  
    * **strikes:**  
        * `amount: 5`  
Number of strikes (incorrect password attempts) a player will receive.
        * `enabled: true`  
Toggle the strike system on/off.
        * `action: kick`  
What happens when a player passes the strike amount?  Valid options are kick and banip.

* **registration:**
    * `enabled: true`  
Toggle new registrations on/off.
    * `forced: true`  
Enable/disable forced registration

* **password:**
    * complexity:
        * `uppercase: false`  
Require at least one uppercase letter in passwords
        * `enabled: false`  
Enable/disable password complexity requirements
        * `symbols: false`  
Require at least one symbol character in passwords
        * `numbers: false`  
Require at least one number in passwords
        * `lowercase: false`  
Require at least one lowercase letter in passwords
    * `min-length: 3`  
Minimum length a players password must be when registering or changing their password.

* **filter:**  
    * `allowed: abcdefghijklmnopqrstuvwxyz0123456789_- ()[]{}`  
Characters that are allowed to be used in a players name.
    * `enabled: true`  
Turn the filter on/off
    * `block-blankname: true`  
Block players with blank names from connecting

* **misc:**
    * `allow-changepw: true`  
Toggle password changes on/off.
    * `allowed-cmds:`  
        * `- /register`  
        * `- /login`  
The commands a player who has not logged may execute.
    * `protect-location: true`  
Whether to conceal a players position until they have logged in by teleporting them to the spawn.
    * `autosave: true`  
Toggle on/off the saving of accounts to file after every registration, password change, and removal of an account.  It's recommended to leave this set to true unless performance issues begin to occur.