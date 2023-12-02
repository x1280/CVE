

# Mastering JavaScript DOM Manipulation: A Guide to Inserting, Replacing, and Removing Child Elements Submitted by oretnom23 has Sensitive Information Leakage

#### BUG_Author: xxxw

#### vendors:

https://www.sourcecodester.com/tutorial/javascript/17023/mastering-javascript-dom-manipulation-guide-inserting-replacing-and

#### description:

If an incorrect database name, username, or password is used, the correct information may be revealed through error messages on the frontend of the website. Attackers could exploit this to obtain critical sensitive information.

use incorrect vistor_log_db, ture database name on the frontend of the website

![image-20231202123818583](https://gitee.com/xw1150/images/raw/master/img/202312021240236.png)

#### the source code /school-visitors-log-e-book/conn /conn.php:

```php
<?php

$servername = "localhost";

$username = "root";

$password = "";

$dbname = "visitors_log_db";

try {

  $conn = new PDO("mysql:host=$servername;dbname=$dbname", $username, $password);

  $conn->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);

} catch(PDOException $e) {

  echo "Connection failed: " . $e->getMessage();

}

?>
```

