## THIS PAGE IS OUTDATED

This page explains how to upgrade to xAuth 2.0 from older versions.

## MAKE SURE TO FOLLOW THE CORRECT GUIDE!

### Upgrading from xAuth v1.0 through v1.2.5 (To MySQL)

1. Download, install, and configure MySQL. Create a MySQL database of xAuth.
2. Delete the old xAuth plugin, config.yml, and strings.yml files.
3. Download the latest version of xAuth, configure the included configuration file, and start your server so the MySQL tables are generated. Stop the server now.
4. Download the flat file to MySQL importer [here] (http://dl.dropbox.com/u/24661378/Bukkit/xAuth/Importer/xAuthImporter%20%28FlatFile%20to%20MySQL%29.zip) and extract all included files into the same directory.
5. Configure the importer.properties file included in the importer to accurately reflect your xAuth configuration.
6. Place your **auths.txt** file in the same directory as the importer.
7. Run the importer (see the bottom of this page for instructions).
8. If no errors are shown, your import should have finished successfully.

***

### Upgrading from xAuth v2.0b4.1 or higher (H2 to H2)

1. Delete the old xAuth plugin, config.yml, messages.yml, and DBVERSION files.
2. Rename **xAuth.h2.db** to **xAuth_old.h2.db**.
3. Download the latest version of xAuth, configure the included configuration file, and start your server so the H2 database is generated. Stop the server now.
4. Download the H2 to H2 importer [here] (http://dl.dropbox.com/u/24661378/Bukkit/xAuth/Importer/xAuthImporter%20%28H2%20to%20H2%29.zip) and extract all included files into the same directory.
5. Configure the importer.properties file included in the importer to accurately reflect your old xAuth configuration.
6. Place **xAuth_old.h2.db** and **xAuth.h2.db** in the same directory as the importer.
7. Run the importer (see the bottom of this page for instructions).
8. If no errors are shown, your import should have finished successfully.
9. Move **xAuth.h2.db** into your xAuth plugins folder.

***

### Upgrading from xAuth v2.0b4.1 or higher (H2 to MySQL)

1. Download, install, and configure MySQL. Create a MySQL database of xAuth.
2. Delete the old xAuth plugin, config.yml, messages.yml, and DBVERSION files.
3. Download the latest version of xAuth, configure the included configuration file, and start your server so the MySQL tables are generated. Stop the server now.
4. Download the H2 to MySQL importer [here] (http://dl.dropbox.com/u/24661378/Bukkit/xAuth/Importer/xAuthImporter%20%28H2%20to%20MySQL%29.zip) and extract all included files into the same directory.
5. Configure the importer.properties file included in the importer to accurately reflect your old and new xAuth configurations.
6. Place the **xAuth.h2.db** file in the same directory as the importer.
7. Run the importer (see the bottom of this page for instructions).
8. If no errors are shown, your import should have finished successfully.

***

### Upgrading from xAuth v2.0b4.1 or higher (MySQL to MySQL)

1. Delete the old xAuth plugin, config.yml, messages.yml, and DBVERSION files.
2. Rename the **accounts** and **sessions** tables in the database used by xAuth to anything other than what the new tables will be named.
3. Download the latest version of xAuth, configure the included configuration file, and start your server so the MySQL tables are generated. Stop the server now.
4. Download the MySQL to MySQL importer [here] (http://dl.dropbox.com/u/24661378/Bukkit/xAuth/Importer/xAuthImporter%20%28MySQL%20to%20MySQL%29.zip) and extract all included files into the same directory.
5. Configure the importer.properties file included in the importer to accurately reflect your old and new xAuth configurations.
6. Run the importer (see the bottom of this page for instructions).
7. If no errors are shown, your import should have finished successfully.

***

###Running the Importer

1. Open Command Prompt (Windows), CLI (*nix), Terminal (Mac).
2. Type `cd path\to\importer` (replace _path\to\importer_ with the actual path on your computer) and press Enter.
3. Type `java -jar xAuthImporter.jar` and press Enter to begin the import process.
