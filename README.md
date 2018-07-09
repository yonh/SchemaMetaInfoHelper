# SchemaMetaInfoHelper
Just A MySQL schema meta data helper class.



## usage

### install
```
composer require 'yonh/schema-meta-info-helper'
```
### example
```PHP
<?php
require __DIR__ . '/vendor/autoload.php';

$host = "localhost";
$user = "root";
$pass = "root";
$port = "3306";
$helper = new \Yonh\SchemaMetaInfoHelper\SchemaMetaInfoHelper($host, $user, $pass, $port);
$tables = $helper->getTables("db_name");
print_r($tables);
```

output
```
Array (
    [test_table] => Array (
            [tableName] => test_table
            [tableComment] => this is a test table
            [columns] => Array (
                    [id] => Array (
                            [name] => id
                            [dataType] => mediumint
                            [type] => mediumint(9)
                            [columnDefault] =>
                            [columnComment] =>
                            [isNullable] =>
                            [autoIncrement] => 1
                        )
                    [name] => Array (
                            [name] => name
                            [dataType] => varchar
                            [type] => varchar(50)
                            [columnDefault] =>
                            [columnComment] => name
                            [isNullable] => 1
                            [autoIncrement] =>
                        )
                )
            [primaryKeys] => Array (
                    [0] => id
                )
            [uniqueIndexs] => Array ( )
        )
)
```
