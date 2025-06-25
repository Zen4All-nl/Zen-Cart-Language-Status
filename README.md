# Set Language Status for Zen Cart
### Version 1.1.0 by Zen4All
Current [Support Thread at Zen Cart Forums](https://www.zen-cart.com/showthread.php?219406-Set-Language-Status-Support-Thread&p=1302587#post1302587)
## Version History:

  - v1.1.0, 2025-06-25, Files updated to Zen Cart 2.1.0
  - v1.0.2, 2017-03-12, Files updated to Zen Cart 1.5.5e
  - v1.0.1, 2016-05-05, Bug release
    - updated \includes\classes\language.php Changed query "and" becomes "where"
  - v1.0.0, 2016-01-28, Initial release

## What it does
The "Set Language Status" module is meant to enable a store owner to enable or disable a language used in his store. At this time if a language is no longer (temporary) needed the only way to disable it, is to delete the language from the database. From the language page in the admin you can enable and disable the languages.
## Installation
There are `core-file overwrites` in this plugin; you should **always** backup your cart&rsquo;s database and files prior to making any changes.

  1. Go to your admin's Tools-&gt;Install SQL Patches; from there you can either upload the install_language_status.sql file or copy and paste the contents of the file.  The contents of the SQL file **assume** that the DB_PREFIX value in your configure.php files is set to blank ('').  If that's not the case, you'll need to edit the .sql file to add your database prefix to the *languages* table's name.  For example, if your DB_PREFIX value is 'zen_', then you would add zen_ to the name of the languages' table (i.e. zen_languages) before running the SQL script.
  2. Make a backup copy of the `overwritten core files`, then copy the plugin's files to your cart, after renaming the "YOUR_TEMPLATE" folder to match your custom template's name and the "YOUR_ADMIN" folder to match your your renamed admin folder's name:
     - /includes/classes/language.php
     - /YOUR_ADMIN/languages.php
     - /YOUR_ADMIN/includes/languages/english/languages.php
## Un-install
Run the **uninstall_language_status.sql** to remove the database entries, then replace the files you previously copied with their initial contents. The contents of the SQL file **assume** that the DB_PREFIX value in your configure.php files is set to blank ('').  If that's not the case, you'll need to edit the .sql file to add your database prefix to the <em>languages</em> table's name. For example, if your DB_PREFIX value is 'zen_', then you would add zen_ to the name of the languages' table (i.e. zen_languages) before running the SQL script.