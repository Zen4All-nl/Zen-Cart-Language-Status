<<<<<<< HEAD
# Zen-Cart-Disable-language
This module will allow you to disable and enable languages instead of deleting.
=======
<h1>Set Language Status for Zen Cart</h1>
<h3>Version 1.0.0 by Zen4All</h3>
<p>Current Support Thread at Zen Cart Forums: <a href="https://www.zen-cart.com/showthread.php?219406-Set-Language-Status-Support-Thread&p=1302587#post1302587">https://www.zen-cart.com/showthread.php?219406-Set-Language-Status-Support-Thread&p=1302587#post1302587</a></p>
<h2>Version History:</h2>
<ul>
<li>v1.0.0, 2016-01-28, Initial release</li>
</ul>
<h2>What it does</h2>
<p>The "Set Language Status" module is meant to enable a store owner to enable or disable a language used in his store. At this time if a language is no longer (temporary) needed the only way to disable it, is to delete the language from the database. From the language page in the admin you can enable and disable the languages.</p>
<h2>Installation</h2>
<p>There are <span class="corefile">core-file overwrites</span> in this plugin; you should <strong>always</strong> backup your cart&rsquo;s database and files prior to making any changes.</p>
<ol>
<li>Go to your admin's Tools-&gt;Install SQL Patches; from there you can either upload the install_language_status.sql file or copy and paste the contents of the file.  The contents of the SQL file <strong>assume</strong> that the DB_PREFIX value in your configure.php files is set to blank ('').  If that's not the case, you'll need to edit the .sql file to add your database prefix to the <em>languages</em> table's name.  For example, if your DB_PREFIX value is 'zen_', then you would add zen_ to the name of the languages' table (i.e. zen_languages) before running the SQL script.</li>
<li>Make a backup copy of the <span class="corefile">overwritten core files</span>, then copy the plugin's files to your cart, after renaming the &quot;YOUR_TEMPLATE&quot; folder to match your custom template's name and the &quot;YOUR_ADMIN&quot; folder to match your your renamed admin folder's name:
<ol>
<li class="corefile">/includes/classes/language.php</li>
<li class="corefile">/YOUR_ADMIN/languages.php</li>
<li class="corefile">/YOUR_ADMIN/includes/languages/english/languages.php</li>
</ol></li>
</ol>
<h2>Un-install</h2>
<p>Run the <strong>uninstall_language_status.sql</strong> to remove the database entries, then replace the files you previously copied with their initial contents. The contents of the SQL file <strong>assume</strong> that the DB_PREFIX value in your configure.php files is set to blank ('').  If that's not the case, you'll need to edit the .sql file to add your database prefix to the <em>languages</em> table's name. For example, if your DB_PREFIX value is 'zen_', then you would add zen_ to the name of the languages' table (i.e. zen_languages) before running the SQL script.</p>
>>>>>>> dev
