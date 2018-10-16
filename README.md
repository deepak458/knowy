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
PHP Validation on Post Value
```php
<?php
// define variables and set to empty values
$name = $email = $gender = $comment = $website = "";

if ($_SERVER["REQUEST_METHOD"] == "POST") {
  $name = test_input($_POST["name"]);
  $email = test_input($_POST["email"]);
  $website = test_input($_POST["website"]);
  $comment = test_input($_POST["comment"]);
  $gender = test_input($_POST["gender"]);
}

function test_input($data) {
  $data = trim($data);
  $data = stripslashes($data);
  $data = htmlspecialchars($data);
  return $data;
}
?>
```
PHP Database Connection Error & Query Error
```php
mysqli_connect_error(); / mysqli_error($conn)
```

Upload a File With PHP

```php
    <form id="form_request_file" method="post" action="index.php" enctype="multipart/form-data">
            <table align="center" width="525" border="0">

               <label for="uploaded" class="control-label col-sm-2">Upload File</label>
                <input id="uploaded"  name="uploaded" type="file"/>
<input value="Submit" name="submit" type="submit"/>
    </form>

<?php
    if(isset($_POST['submit'])){
     if(isset($_FILES['uploaded'])){
        $path = "uploaded_docs/";  
        $file_name = basename( $_FILES['uploaded']['name']);
        $target = $path . $file_name ;      
    if(move_uploaded_file($_FILES["uploaded"]["tmp_name"], $target)){ 
            echo $file_name." was uploaded";
    }else{
            echo "Could not upload";
    }
    }
?>
```

CURL Code
```php
<?php
if (! function_exists ( 'curl_version' )) {
    exit ( "Enable cURL in PHP" );
}

$ch = curl_init ();
$timeout = 0; // 100; // set to zero for no timeout
$myHITurl = "http://www.google.com";
curl_setopt ( $ch, CURLOPT_URL, $myHITurl );
curl_setopt ( $ch, CURLOPT_HEADER, 0 );
curl_setopt ( $ch, CURLOPT_RETURNTRANSFER, 1 );
curl_setopt ( $ch, CURLOPT_CONNECTTIMEOUT, $timeout );
$file_contents = curl_exec ( $ch );
if (curl_errno ( $ch )) {
    echo curl_error ( $ch );
    curl_close ( $ch );
    exit ();
}
curl_close ( $ch );

// dump output of api if you want during test
echo "$file_contents";
?>
```


