This page explains how to upgrade to xAuth 2.0 from various previous versions.

***

### Upgrading from xAuth v1.0 through v1.2.5

1. Download the latest version of xAuth, configure the included configuration file, and start your server so the MySQL tables are generated. Stop the server now.
2. Download the flat file importer [here] (http://bit.ly/A9OZT9) and extract all included files into the same directory.
3. Configure the importer.properties file included in the importer to accurately reflect your xAuth configuration.
4. Place your _auths.txt_ file in the same directory as the importer.
5. Run the importer:
    - **Windows**:
        1. Open Command Prompt, type `cd path\to\importer` and hit enter.
        2. Now do the same for `java -jar xAuthImporter.jar` to begin the import process.
    - **Linux**:
        1. Navigate to the directory xAuthImporter.jar is located in.
        2. Execute `java -jar xAuthImporter.jar` to begin the import process.
6. If no errors are shown, your import should have finished successfully.

***

### Upgrading from xAuth v2.0b4.1 or higher (H2)

1. Download the latest version of xAuth, configure the included configuration file, and start your server so the MySQL tables are generated. Stop the server now.
2. Download the H2 importer [here] (http://bit.ly/zs7Btd) and extract all included files into the same directory.
3. Configure the importer.properties file included in the importer to accurately reflect your old and new xAuth configurations.
4. Place your _xAuth.h2.db_ file in the same directory as the importer.
5. Run the importer:
    - **Windows**:
        1. Open Command Prompt, type `cd path\to\importer` and hit enter.
        2. Now do the same for `java -jar xAuthImporter.jar` to begin the import process.
    - **Linux**:
        1. Navigate to the directory xAuthImporter.jar is located in.
        2. Execute `java -jar xAuthImporter.jar` to begin the import process.
6. If no errors are shown, your import should have finished successfully.

***

### Upgrading from xAuth v2.0b4.1 or higher (MySQL)

1. Rename the **accounts** and **sessions** tables in your current database to anything other than what the new tables will be named.
2. Download the latest version of xAuth, configure the included configuration file, and start your server so the MySQL tables are generated. Stop the server now.
3. Download the MySQL importer [here] (http://bit.ly/Am1jJ6) and extract all included files into the same directory.
4. Configure the importer.properties file included in the importer to accurately reflect your old and new xAuth configurations.
5. Run the importer:
    - **Windows**:
        1. Open Command Prompt, type `cd path\to\importer` and hit enter.
        2. Now do the same for `java -jar xAuthImporter.jar` to begin the import process.
    - **Linux**:
        1. Navigate to the directory xAuthImporter.jar is located in.
        2. Execute `java -jar xAuthImporter.jar` to begin the import process.
6. If no errors are shown, your import should have finished successfully.