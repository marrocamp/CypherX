| Node | Field | Type | Default Value |
|------|-------|------|---------------|
| main.datasource | datasource | String | default|
| main.auto-disable | autoDisable | Boolean | true |
| main.reverse-enforce-single-session | reverseESS | Boolean | true |

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