# UPDATE VARBASE STEPS
Steps on updating varbase installation.

1. Check current "Varbase-project" composer.json file. If they are old, use the links below to get the latest files.
  * Composer.json file link: https://github.com/Vardot/varbase-project/blob/8.4.x/composer.json
  * Varbase project link: https://www.drupal.org/project/varbase
2. Go into your drupal docroot folder and delete the all the files except the following folders:
  * files 
  * libraries 
  * modules 
  * sites 
  * themes
3. Copy all the files from the new files from the varbase update into the project docroot except the following folders:
  * modules
  * sites
  * themes
4. Go to the project root folder and not the docroot.
5. Delete "vendor" folder.
6. Delete "composer.lock" file
7. Run "composer require vardot/varbase:8.4.14" command.
  * Note: the varbase version number will change depending of the release number
8. Wait for composer to finish.
  * Note: if error found when downloading a patch, redo step 7.
  * If no issues are found the terminal should display "Writing lock file" and "Generating autoload files"
10. Log into the site as an admin.
11. Run drush "updb" or just go to "/update.php" on your site.
12. Wait for the database update to finish.
13. If "Features" and "Features UI" modules not enable, enable them.
14. Go to "admin/config/development/features"
15. Click on all the "Changed" tags for each module.
16. Select all the differences and import them.
17. Congratulations you have updated to the latest varbase \(^ ^)/ CHEERS!!!
