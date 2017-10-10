# SchemaMetaInfoHelper
mysql schema meta data helper



## usage

### install
```
composer require 'yonh/schema-meta-info-helper'
```
### example
```PHP
$host = "localhost";
$user = "root";
$pass = "root";
$port = "3306";
$helper = new Yonh\SchemaMetaInfoHelper\SchemaMetaInfoHelper($host, $user, $pass, $port);
$tables = $helper->getTables("db_name");
print_r($tables);
```
