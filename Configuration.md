xAuth has many configurable settings that let you, the server manager, have nearly complete control over how it operates.  To begin configuring, first navigate to the /plugins/xAuth/ directory and open config.yml in a text editor of your choice.  

The configuration is divided up into nodes that each have one or multiple properties for easier management.  A description of these nodes and properties is below.

***
* **session:**
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

* **registration:**
    * `enabled: true`  
Toggle new registrations on/off.
    * `pw-min-length: 3`  
Minimum length a players password must be when registering or changing their password.

* **misc:**
    * `allow-changepw: true`  
Toggle password changes on/off.
    * `allowed-cmds:`  
        * `- /register`  
        * `- /login`  
The commands a player who has not logged may execute.
    * `autosave: true`  
Toggle on/off the saving of accounts to file after every registration, password change, and removal of an account.  It's recommended to leave this set to true unless performance issues begin to occur.