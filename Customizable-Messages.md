<pre><code>join:
    register: '{RED}You are not registered.{NEWLINE}{RED}Please register using /register <password>.'
    login: '{RED}Please log in using /login <password>.'
    resume: '{BRIGHTGREEN}Welcome back, your login session has been resumed.'
    error:
        lockout: 'You are temporarily locked out for exceeding the incorrect password threshold.'
        name: 'Your name contains one or more illegal characters.'

register:
    usage: '{RED}Correct Usage: /register <password> [email]'
    success: '{BRIGHTGREEN}You have successfully registered!{NEWLINE}{BRIGHTGREEN}You may now log in using /login <password>'
    error:
        disabled: '{RED}Registrations are currently disabled!'
        registered: '{RED}You are already registered!'
        limit: '{RED}You may not register any more accounts!'
        password: '{RED}Your password must be at least {PWMINLENGTH} characters long!'
        email: '{RED}Please use a valid email address when registering!'
        general: '{RED}Something went wrong while creating your account!'

login:
    usage: '{RED}Correct Usage: /login <password>'
    success: '{BRIGHTGREEN}You are now logged in!'
    error:
        registered: '{RED}You are not registered!'
        authenticated: '{RED}You are already logged in!'
        password: '{RED}Incorrect password!'
        active: '{RED}Your account is not activated!'
        general: '{RED}Something went wrong while logging you in!'

logout:
    success: '{BRIGHTGREEN}You have been logged out!'
    error:
        logged: '{RED}You are not logged in!'
        general: '{RED}Something went wrong while logging you out!'

changepw:
    usage: '{RED}Correct Usage: /changepw <old password> <new password>'
    success: '{BRIGHTGREEN}Password changed!'
    error:
        disabled: '{RED}Password changes are currently disabled.'
        logged: '{RED}You are not logged in!'
        incorrect: '{RED}Incorrect old password!'
        invalid: '{RED}Your new password does not meet complexity requirements!'
        general: '{RED}Something went wrong while changing your password!'

authurl:
    registration: '{RED}AuthURL registration is disabled.'
    changepw: '{RED}AuthURL does not support password changes.'

misc:
    illegal: '{GRAY}You must be logged in to do that!'
    timeout: 'You have taken too long to log in!'
    strikeout: 'You have entered too many invalid passwords!'
    reloaded: '{RED}Server reloaded, you must log in.'

admin:
    permissions: 'You do not have permission to use this command!'
    register:
        usage: '{RED}Correct Usage: /xauth register <player> <password> [email]'
        success: '{BRIGHTGREEN}Account successfully created for: {WHITE}{TARGET}'
        error:
            registered: '{RED}This player is already registered!'
            general: '{RED}Something went wrong while creating an account for {TARGET}'
    changepw:
        usage: '{RED}Correct Usage: /xauth changepw <player> <new password>'
        success: '{TARGET}''s {BRIGHTGREEN}password has been changed!'
        error:
            registered: '{RED}This player is not registered!'
            general: '{RED}Something went wrong while changing {TARGET}''s pasword!'
    logout:
        usage: '{RED}Correct Usage: /xauth logout <player>'
        error:
            logged: '{TARGET} {RED}is not logged in!'
            general: '{RED}Something went wrong while logging this player out!'
        success:
            player: '{TARGET} {BRIGHTGREEN}has been logged out!'
            target: '{BRIGHTGREEN}You have been logged out by an Administrator!'
    unregister:
        usage: '{RED}Correct Usage: /xauth unregister <player>'
        error:
            registered: '{RED}This player is not registered!'
            general: '{RED}Something went wrong while unregistering this player!'
        success:
            player: '{TARGET} {BRIGHTGREEN}has been unregistered!'
            target: '{RED}You have been unregistered and logged out!'
    location:
        usage: '{RED}Correct Usage: /xauth location set|remove [global]'
        set:
            error:
                global: '{RED}Global teleport location is set to this world.{NEWLINE}{RED}Please remove it first.'
                general: '{RED}Something went wrong while setting this location!'
            success:
                regular: '{BRIGHTGREEN}Teleport location for this world set to your location!'
                global: '{BRIGHTGREEN}Global teleport location set to your location!'
        remove:
            error:
                noglobal: '{RED}A global teleport location is not set!'
                notset: '{RED}This world does not have a teleport location!'
                global: '{RED}Global teleport location is set to this world.{NEWLINE}{RED}Please use /xauth location remove global'
                general: '{RED}Something went wrong while removing this location!'
            success:
                regular: '{BRIGHTGREEN}Teleport location for this world has been removed!'
                global: '{BRIGHTGREEN}Global teleport location has been removed!'</code></pre>

***
**String Replacements**

<pre><code>For all colors see: http://www.minecraftwiki.net/wiki/Classic_server_protocol#Color_Codes

{BLACK}
{DARKBLUE}
{DARKGREEN}
{DARKTEAL}
{DARKRED}
{PURPLE}
{GOLD}
{GRAY}
{DARKGRAY}
{BLUE}
{BRIGHTGREEN}
{TEAL}
{RED}
{PINK}
{YELLOW}
{WHITE}

{PLAYER} - Name of the player the message is being sent to

{TARGET} - Name of the target player in admin commands

{PWMINLENGTH} - Password minimum length

{NEWLINE} - Split a message into multiple lines</code></pre>