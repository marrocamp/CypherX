**Problem:**  
org.h2.jdbc.JdbcSQLException: Column "IF" not found

**Explanation:**
You're using an older version of the H2 database library that doesn't support one of the newer features that xAuth uses.

**Solution:**
Replace the H2 database library file located in _server root/lib_ with "this":http://dl.dropbox.com/u/24661378/Bukkit/lib/h2.jar one and restart the server.