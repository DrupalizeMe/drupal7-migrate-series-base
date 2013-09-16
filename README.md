This repository contains Drupal 7 and the various modules used as part of the [Drupalize.Me](http://drupalize.me) video series on Drupal 7's [Migrate module](http://drupal.org/project/migrate). This is intended to be used as a starting point for people following along with the lessons in the series and also contains database snapshots for lessons where we have made modifications to the database.

**Usage**

Download or clone this repository and copy `docroot/sites/default/default.settings.php` to `docroot/sites/default/settings.php` and then edit the new settings.php file to provide your database credentials.

There are SQL files in the `data/` directory which contain snapshots of the database at various points throughout the series. Generally taken at the end of each lesson for which it's numbered.

The admin username and password used to login to drupal is:

- Username: admin
- Password: admin

These snapshots can be imported like so:

`gunzip < data/drupal-7.sql.gz | mysql -u username - p password -h localhost myd7_database`

Or with just about any database management tool.

If you are following along with the series the code for the sportsball module that is being written can be found here https://github.com/DrupalizeMe/sportsball.

If you're simply looking at this as an example note that the sportsball module needs to be added into the `docroot/sites/default/modules/custom` directory as that's where the included database snapshots assume it will be located.