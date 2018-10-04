

1. How to GET Page URL in PHP

$URL = (isset($_SERVER['HTTPS']) && $_SERVER['HTTPS'] === 'on' ? "https" : "http") . "://$_SERVER[HTTP_HOST]$_SERVER[REQUEST_URI]";

2. How to Allow Error Reporting in PHP
ini_set('display_errors', 1);
ini_set('display_startup_errors', 1);
error_reporting(E_ALL);
display_errors = on

3. PHP Post Server Request
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
     // The request is using the POST method
}

4. Array First Key Value
reset($array);
$first_key = key($array);

5. Setting Header for Json Value
header('Content-Type: application/json');

**https://stackoverflow.com/questions/3737139/reference-what-does-this-symbol-mean-in-php


Exest 8 letter
sprintf('%08d', 1234567);

 
Time Out Function
ini_set('max_execution_time', 300); //300 seconds = 5 minutes


