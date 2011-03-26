Replacement variables is (currently) an extremely basic method used to replace part of a string with a dynamic variable such as a player name.  Five of the current customizable strings allow replacement variables and are detailed below.

* register.err.password
    * %1 - value of config.yml node register.pw-min-length
* register.success2
    * %1 - password the player has registered with
* changepw.success.self
    * %1 - players new password
* unregister.success
    * %1 - name of player who has been unregistered
* toggle.success.*
    * %1 - "enabled" or "disabled"