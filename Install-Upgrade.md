### Installing a fresh copy of xAuth
1. Download the latest version and place/extract it in your /plugins/ directory.
2. (Default Datasource) The [H2 Database Engine Library](https://github.com/downloads/CypherX/xAuth/h2.jar) is required if MySQL is not being used. Download and place it in the /lib/ directory located in your server root. (If this directory does not exist you must create it)
2. (MySQL) Create a database (it can be named whatever you want) and fill out the MySQL section of the configuration file.
3. Start your server and the xAuth configuration files should be created automatically if they do not already exist.

***
### Upgrading to xAuth v2
1. Download the latest version and place it in your /plugins/ directory.
2. Delete/rename the old config.yml and strings.yml so the new ones can be created.
3. The [H2 Database Engine Library](https://github.com/downloads/CypherX/xAuth/h2.jar) is required if MySQL is not being used. Download and place it in the /lib/ directory located in your server root. (If this directory does not exist you must create it)
4. When the server is started, the new configuration files will be created and auths.txt will be imported to the new format.
