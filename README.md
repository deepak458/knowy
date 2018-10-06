# PHP Help for Code

How to GET Page URL in PHP
```php
$url = (isset($_SERVER['HTTPS']) && $_SERVER['HTTPS'] === 'on' ? "https" : "http")."://$_SERVER[HTTP_HOST]$_SERVER[REQUEST_URI]";
```

How to Allow Error Reporting in PHP
```php
ini_set('display_errors', 1);
ini_set('display_startup_errors', 1);
error_reporting(E_ALL);
display_errors = on
```

PHP Post Server Request
```php
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
     // The request is using the POST method
}
```

Array First Key Value
```php
reset($array);
$first_key = key($array);
```

Setting Header for Json Value `header('Content-Type: application/json')`

[All Symbol in PHP](https://stackoverflow.com/questions/3737139/reference-what-does-this-symbol-mean-in-php)

Exest 8 letter
```php
sprintf('%08d', 1234567);
```
 
Time Out Function
```php
ini_set('max_execution_time', 300); //300 seconds = 5 minutes
```

PHP Insert Mysqli id
```php
$id = mysqli_insert_id($con);
```
