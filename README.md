# PDO connection boilerplate
How to connect to PDO

```
$db_server = 'localhost';
$db_port = '3306';
$db_name = 'test';
$db_user = 'user';
$db_pass = 'pass';

$dsn = 'mysql:host=' . $db_server . ';dbname=' . $db_name . ';port=' . $db_port;
$driver_options = [
   PDO::MYSQL_ATTR_INIT_COMMAND => "SET NAMES 'utf8'",
   PDO::ATTR_ERRMODE => PDO::ERRMODE_EXCEPTION,
   PDO::ATTR_DEFAULT_FETCH_MODE => PDO::FETCH_ASSOC,
];               
$dbh = new PDO( $dsn, $db_user, $db_pass, $driver_options );
```
