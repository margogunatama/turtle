# 9/25/2017

Another subversion is being released. This introduces a few major changes to the CRUD generator, permissions, views, etc. After using Turtle for a number of my own projects I have found that CRUD is not sufficient enough, and confuses the end-user a bit. Therefore, after looking at Voyager, I've decided to change CRUD to BREAD. This is more clear to users ("add" is less confusing than "create"), and the additional "browse" permission is essential for separating browse/read concerns.

Changes in this release:

* CRUD has been replaced with BREAD
* Non-modal forms now use cards
* Added `reload_sources` AJAX response functionality

# 9/20/2017

Introducing a changelog :)

Subversion 1.1.0 is going to introduce a few fixes and path name changes, so be sure to update the existing `required` tag files accordingly.

The new file paths are as follows:

```
config/turtle.php
resources/views/vendor/turtle/layouts/app.blade.php
public/turtle/*.*
```

They used to be:

```
config/turtle.php
resources/views/kjdion84/turtle/layouts/app.blade.php
public/kjdion84/turtle/*.*
```

This is to ensure they are in line with Laravel best practices.

Changes in this release:

* Removed migration publishing, please create your own migrations using newer timestamps if you want to tweak the package database migrations after they run
* Fixed view file publishing - it was using the wrong path so view customization was not working correctly
* Fixed `App\User` so you can actually use your own Auth User class now via the config file