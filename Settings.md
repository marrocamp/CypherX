|Node|Field|Type|Default Value|Description|
|----|-----|----|-------------|-----------|
|main.datasource|datasource|String|default|System of data persistence xAuth will use.<br />Values: default, mysql|
|main.auto-disable|autoDisable|Boolean|true|If set to true, xAuth will disable itself if the server is running in online-mode.|
|main.reverse-enforce-single-session|reverseESS|Boolean|true|Kicks the player connecting if a player with the same name is already online.|
|mysql.host|mysqlHost|String|localhost|Location of the MySQL server. Can be either a host name or IP address.|
|mysql.port|mysqlPort|Integer|3306|Port used by the MySQL server.
|mysql.username|mysqlUser|String|root|User name used to connect to the MySQL server.|
|mysql.password|mysqlPass|String||Password used to connect to the MySQL server.|
|mysql.database|mysqlDb|String||Name of the database that will be used by xAuth.|
|mysql.tables.account|tblAccount|String|accounts|Name of the table that player accounts will be stored in.|
|mysql.tables.session|tblSession|String|sessions|Name of the table that player sessions will be stored in.|
|mysql.tables.strike|tblStrike|String|strike_bans|Name of the table that strike system bans will be stored in.|
|mysql.tables.location|tblLocation|String|tele_locations|Name of the table that teleport locations will be stored in.|
|mysql.tables.inventory|tblInventory|String|inventory|Name of the table that player inventories will be stored in.|
|registration.enabled|regEnabled|Boolean|true|Turn on/off new registrations.|
|registration.forced|regForced|Boolean|true|If set to true, all players will be forced to register.|
|registration.require-email|requireEmail|Boolean|false|Setting this to true requires a player to enter an email address upon registration.|
|registration.validate-email|validateEmail|Boolean|true|If set to true, email addresses will be checked for validity.|
|registration.allow-multiple|allowMultiple|Boolean|true|Setting this to false will impose a limit of one account per IP address.|
|registration.activation|activation|Boolean|false|Used with web registrations that require account activation.|
|login.strikes.amount|maxStrikes|Integer|5|Amount of times a player can enter an incorrect password before action is taken.<br />Set to 0 to disable.|
|login.strikes.action|strikeAction|String|kick|What action to take when the strike threshold is reached.<br />Values: kick, banip|
|login.strikes.length|banLength|Integer|3600|Length, in seconds, of a ban given by the strike system.<br />Set to 0 for a permanent ban.|
|password.min-length|pwMinLength|Integer|6|Minimum length of a valid password.|
|password.allow-change|pwAllowChange|Boolean|true|Enable/disable password changes.|
|password.complexity.lowercase|pwCompLower|Boolean|false|If set to true, passwords will require at least one lowercase character.|
|password.complexity.uppercase|pwCompUpper|Boolean|false|If set to true, passwords will require at least one uppercase character.|
|password.complexity.number|pwCompNumber|Boolean|false|If set to true, passwords will require at least one numerical character.|
|password.complexity.symbol|pwCompSymbol|Boolean|false|If set to true, passwords will require at least one special character.|
|guest.timeout|guestTimeout|Integer|300|Amount of time, in seconds, that a player has to log in before they are kicked.<br />Set as 0 to disable.|
|guest.notify-cooldown|notifyCooldown|Integer|5|Amount of time, in seconds, between "You must be logged in.." messages.|
|guest.allowed-commands|allowedCmds|String List|[register, login, l]|Commands that players who are not registered or logged in may execute.|
|session.length|sessionLength|Integer|3600|Amount of time, in seconds, that a session will remain valid.|
|session.verifyip|verifyIp|Boolean|true|Verify a player's IP address when resuming a session.|
|session.godmode-length|godmodeLength|Integer|5|Length of time, in seconds, that a player will have godmode upon logging in.<br />Set to 0 to disable.
|filter.min-length|filterMinLength|Integer|2|Minimum length a players name can be.|
|filter.allowed|filterAllowed|String|'*'|Characters that may be present in a players name. Use an asterisk (*) to allow all.|
|filter.blankname|filterBlank|Boolean|true|If set to false, players with blank names can connect to the server.|

<pre><code>#
# Configuration file for xAuth
#

main:
    # How should xAuth store data (Accounts, sessions, etc.)?
    # Possible values: default (H2), mysql
    datasource: default
    # If set to true, xAuth will disable itself if the server is in online-mode
    auto-disable: true
    # When set to true, if a player connects with the same name as someone who is
    # already online, the player connecting will be kicked instead of the online player
    reverse-enforce-single-session: true

mysql:
    # Location of the MySQL server. Can be either a host name or IP address
    host: localhost
    # Port used by MySQL. Default is 3306
    port: 3306
    # User name used to connect to the MySQL server
    username: root
    # Password used to connect to the MySQL server
    password: 
    # Name of the database that will be used by xAuth
    database: 
    # Names of the tables xAuth will use to store data
    tables:
        account: accounts
        session: sessions
        strike: strike_bans
        location: tele_locations

registration:
    # Enable/disable new registrations
    enabled: true
    # If set to true, everyone must register
    forced: true
    # Setting this to true requires a player to enter an email address when they register
    require-email: false
    # If set to true, a valid email address is required
    validate-email: true
    # Setting this to false will impose a limit of one account per IP address
    allow-multiple: true
    # Used with web registrations that require account activation
    activation: false

login:
    strikes:
        # Amount of times a player can enter an incorrect password before action is taken
        # Set as 0 to disable
        amount: 5
        # What action to take when the strike threshold is reached
        # Possible values: kick, banip
        action: kick
        # Length, in seconds, of a ban given by the strike system
        # Set as 0 for a permanent ban
        length: 3600

password:
    # Minimum length a password may be
    min-length: 6
    # Enable/disable password changes
    allow-change: true
    # Require at least one of the character types below that are set to true
    complexity:
        lowercase: false
        uppercase: false
        number: false
        symbol: false

guest:
    # Amount of time, in seconds, that a player has to log in before they are kicked
    # Set as 0 to disable
    timeout: 300
    # Amount of time, in seconds, between "You must be logged in.." messages
    notify-cooldown: 5

session:
    # Amount of time, in seconds, that a session will remain valid
    length: 3600
    # Verify a player's IP address when resuming a session
    verifyip: true
    # Length of time, in seconds, that a player will have godmode upon logging in
    # set as 0 to disable
    godmode-length: 5

filter:
    # Minimum length a players name can be
    min-length: 2
    # Characters that may be present in a players name. Use an asterisk (*) to allow all
    allowed: '*'
    # If set to false, players with blank names can connect
    blankname: true

# INTERNAL USE ONLY! DO NOT TOUCH!
version: 1</code></pre>