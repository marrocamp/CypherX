**Problem:**  
`org.h2.jdbc.JdbcSQLException: Column "IF" not found`

**Explanation:**  
You're using an older version of the H2 database library that doesn't support one of the newer features that xAuth uses.

**Solution:**  
Replace the H2 database library file located in _server root/lib_ with [this](http://dl.dropbox.com/u/24661378/Bukkit/lib/h2.jar) one and restart the server.
***
**Problem:**
`org.h2.jdbc.JdbcSQLException: Table "STRIKES" not found`

**Explanation:**  
There are two reasons why this error might occur.  The table used to store strike information is missing from the database **OR** the name of said table in the configuration is incorrect.

**Solution:**
Open the xAuth configuration file and change the value of _mysql.tables.strike_ to 'strike_bans' (without the quotes) and restart the server.  If this does not solve your problem, follow the instructions below.

1. [Start the H2 Console](http://www.h2database.com/html/tutorial.html#tutorial_starting_h2_console) (the server must be stopped).
2. Connect to the xAuth database by changing 'JDBC URL' to the location of the xAuth database and putting 'sa' (no quotes) in the 'User Name' field, then click connect.
3. If you've successfully connected to the database, there should be a list of tables on the left side.  Make a post in the xAuth thread on the Bukkit forum containing a list or screenshot of these tables.