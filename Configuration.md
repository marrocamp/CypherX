|Node|Type|Default Value|Description|
|----|----|-------------|-----------|
|main.auto-disable|Boolean|true|If set to true, xAuth will disable itself if the server is running in online-mode.|
|main.check-for-updates|Boolean|true|Toggle automatic checking for updates.|
|main.download-library|Boolean|true|If set to true, xAuth will automatically download the required H2 library if it does not exist.|
|main.reload-on-join|Boolean|true|Turn on/off reloading of cached player data when a player connects.|
|mysql.enabled|Boolean|false|Use MySQL?|
|mysql.host|String|localhost|Location of the MySQL server. Can be either a host name or IP address.|
|mysql.port|Integer|3306|Port used by the MySQL server.
|mysql.user|String|user|User name used to connect to the MySQL server.|
|mysql.password|String|password|Password used to connect to the MySQL server.|
|mysql.database|String|xauth|Name of the database that will be used by xAuth.|
|mysql.tables.account|String|accounts|Name of the table that player accounts will be stored in.|
|mysql.tables.location|String|locations|Name of the table that teleport locations will be stored in.|
|mysql.tables.lockout|String|lockouts|Name of the table that strike system lockouts will be stored in.|
|mysql.tables.playerdata|String|playerdata|Name of the table that player inventories and locations will be stored in.|
|mysql.tables.session|String|sessions|Name of the table that player sessions will be stored in.|
|authurl.enabled|Boolean|false|Turn on/off authentication over URL.|
|authurl.url|String|http://google.com|URL used by AuthURL.|
|authurl.registration|Boolean|false|Turn on/off AuthURL registrations.|
|authurl.status|Boolean|false|Turn on/off AuthURL online/offline status updates.|
|authurl.groups|Boolean|false|Turn on/off AuthURL permission group settings.|
|authurl.broadcast-login|Boolean|false|Turn on/off global notifications when a player logins|
|single-session.reverse|Boolean|true|Enable reverse-enforce-single-session for authenticated players.|
|single-session.guests.reverse|Boolean|false|Enable reverse-enforce-single-session for non-logged in players.|
|single-session.guests.immunity-length|Integer|5|Length of time, in seconds, that non-logged in players will be immune to being disconnected by another player with the same name if guest reverse is disabled.|
|registration.enabled|Boolean|true|Turn on/off new registrations.|
|registration.forced|Boolean|true|If set to true, all players will be forced to register.|
|registration.require-email|Boolean|false|Setting this to true requires a player to enter an email address upon registration.|
|registration.validate-email|Boolean|true|If set to true, email addresses will be checked for validity.|
|registration.account-limit|Integer|1|Controls how many accounts a specific IP address can register.|
|registration.activation|Boolean|false|Used with web registrations that require account activation.|
|registration.require-login|Boolean|true|Controls whether logging in after registering is required.|
|password.min-length|Integer|6|Minimum length of a valid password.|
|password.allow-change|Boolean|true|Enable/disable password changes.|
|password.complexity.lowercase|Boolean|false|If set to true, passwords will require at least one lowercase character.|
|password.complexity.uppercase|Boolean|false|If set to true, passwords will require at least one uppercase character.|
|password.complexity.number|Boolean|false|If set to true, passwords will require at least one numerical character.|
|password.complexity.symbol|Boolean|false|If set to true, passwords will require at least one special character.|
|guest.timeout|Integer|300|Amount of time, in seconds, that a player has to log in before they are kicked.<br />Set as 0 to disable.|
|guest.notify-cooldown|Integer|5|Amount of time, in seconds, between "You must be logged in.." messages.|
|guest.hide-inventory|Boolean|true|Turn on/off inventory hiding|
|guest.protect-location|Boolean|true|Turn on/off location protection|
|guest.allowed-commands|String List|[register, login, l]|Commands that players who are not registered or logged in may execute.|
|guest.restrict.player.chat|Boolean|true|Allow/disallow a player from chatting while they are not logged in.|
|guest.restrict.player.interact|Boolean|true|Allow/disallow a player from interacting with levers, switches, etc. while they are not logged in.|
|guest.restrict.player.move|Boolean|true|Allow/disallow a player from moving while they are not logged in.|
|guest.restrict.player.pickup|Boolean|true|Allow/disallow a player from picking up items while they are not logged in.|
|guest.restrict.block.place|Boolean|true|Allow/disallow a player from placing blocks while they are not logged in.|
|guest.restrict.block.break|Boolean|true|Allow/disallow a player from breaking blocks while they are not logged in.|
|guest.restrict.entity.damage|Boolean|true|Allow/disallow a player from giving and receiving damage while they are not logged in.|
|guest.restrict.entity.target|Boolean|true|Allow/disallow a player from being targeted (followed) by mobs while they are not logged in.|
|session.length|Integer|3600|Amount of time, in seconds, that a session will remain valid.|
|session.verifyip|Boolean|true|Verify a player's IP address when resuming a session.|
|session.godmode-length|Integer|5|Length of time, in seconds, that a player will have godmode upon logging in.<br />Set to 0 to disable.|
|strikes.amount|Integer|5|Amount of times a player can enter an incorrect password before action is taken.<br />Set to 0 to disable.|
|strikes.lockout-length|Integer|3600|Length of time, in seconds, that a player will be locked out after passing the strike threshold.<br />Set to 0 for a permanent ban.|
|account.track-last-login|Boolean|false|If set to true, the lastloginip and lastlogindate database fields will be updated.|
|filter.min-length|Integer|2|Minimum length a players name can be.|
|filter.allowed|String||Characters that may be present in a players name.|
|filter.disallowed|String||Characters that may NOT be present in a players name.|
|filter.blank-name|Boolean|true|If set to false, players with blank names can connect to the server.|

<pre><code>main:
  auto-disable: true
  check-for-updates: true
  download-library: true
  reload-on-join: false
mysql:
  enabled: false
  host: localhost
  port: 3306
  user: user
  password: password
  database: xauth
  tables:
    account: accounts
    location: locations
    lockout: lockouts
    playerdata: playerdata
    session: sessions
authurl:
  enabled: false
  url: http://google.com
  registration: false
  status: false
  groups: false
  broadcast-login: false
single-session:
  reverse: true
  guests:
    reverse: false
    immunity-length: 5
registration:
  enabled: true
  forced: true
  require-email: false
  validate-email: false
  account-limit: 0
  activation: false
  require-login: true
password:
  min-length: 6
  allow-change: true
  complexity:
    lowercase: false
    uppercase: false
    number: false
    symbol: false
guest:
  timeout: 300
  notify-cooldown: 5
  hide-inventory: true
  protect-location: true
  allowed-commands:
  - register
  - login
  - l
  restrict:
    player:
      chat: true
      interact: true
      move: true
      pickup: true
    block:
      place: true
      break: true
    entity:
      damage: true
      target: true
session:
  length: 3600
  verifyip: true
  godmode-length: 5
strikes:
  amount: 5
  lockout-length: 3600
account:
  track-last-login: false
filter:
  min-length: 2
  allowed: ''
  disallowed: ''
  blank-name: true</code></pre>