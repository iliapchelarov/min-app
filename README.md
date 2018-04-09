<p align="center">
    <a href="https://github.com/yiisoft" target="_blank">
        <img src="https://avatars0.githubusercontent.com/u/993323" height="100px">
    </a>
    <h1 align="center">Yii minimal Project Template</h1>
    <a rel="author" href="https://github.com/iliapchelarov">Author: Ilia Pchelarov </a>
    <br>
</p>

Yii 2 minimal Project Template is a skeleton [Yii 2](http://www.yiiframework.com/) application best for
rapidly creating small projects.


DIRECTORY STRUCTURE
-------------------

      config/             contains application configurations
      src/                contains model classes
      runtime/            contains files generated during runtime e.g. logs
      tests/              contains tests for the application
      vendor/             contains dependent 3rd-party packages installed via composer

REQUIREMENTS
------------

The minimum requirement by this project template that your Web server supports PHP 5.4.0.


INSTALLATION
------------

### Install via Composer

If you do not have [Composer](http://getcomposer.org/), you may install it by following the instructions
at [getcomposer.org](http://getcomposer.org/doc/00-intro.md#installation-nix).

You can then install this project template using the following command:

~~~
composer create-project --prefer-dist --stability=dev ipchelarov/min-app basic
~~~

CONFIGURATION
-------------

### Database

Edit the file `config/db.php` with real data, for example:

```php
return [
    'class' => 'yii\db\Connection',
    'dsn' => 'mysql:host=localhost;dbname=yii2basic',
    'username' => 'root',
    'password' => '1234',
    'charset' => 'utf8',
];
```

For testing purposes edit the file `config/test_db.php` to use SQLite:
```php
    $db['dsn'] = 'sqlite:@app/sqlite';
```

### Aliases & Autoloading

In the above code `@app` is an Yii defined alias for the application directory i.e ./
For aliases to work, you need to bootstrap the Yii framework first by including Yii.php in the autoloading process.
See example in the './yii' boot script:

```php
require __DIR__ . '/vendor/yiisoft/yii2/Yii.php';
```

**NOTES:**
- Yii won't create the database for you, this has to be done manually before you can access it.
- Check and edit the other files in the `config/` directory to customize your application as required.
- Refer to the README in the `tests` directory for information specific to basic application tests.


TESTING
-------

Tests are located in `tests` directory. They are developed with [PHPUnit Testing Framework](https://phpunit.de/).

Tests can be executed by running

```
./vendor/bin/phpunit --bootstrap tests/_bootstrap.php tests
```
or by using the utility script
```
./test
```

The command above will execute all unit tests located in the directory `tests`. Unit tests are testing the system components and simple integration scenarios.
They are basic system health-check, but not a replacement for user interaction (functional) - and acceptance tests. 

Enjoy!
------