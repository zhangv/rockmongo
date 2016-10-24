Introduction
--------------------------------------
RockMongo is a MongoDB administration tool, written in PHP 5, very easy to install and use.


Installation
--------------------------------------
Please check out https://github.com/iwind/rockmongo/ to find everything there.

3 Steps
--------------------------------------
0. Make sure you have upgrade to the PHP7.0+ and Composer is ready to use.
1. Install upgraded Mongodb extension: composer require mongodb/mongodb
   Install the genius adapter: composer require alcaeus/mongo-php-adapter
2. In the rockmongo/index.php, add the composer loader on the top, something like:
``$loader = require 'path/to/vendor/autoload.php';
   In the rockmongo/app/controllers/server.php, find the line containing: ``$this->directives = ini_get_all("mongo");
   and change it to ``$this->directives = ini_get_all("mongodb");
   as the extension name is changed after the upgrade.
   
Done!
