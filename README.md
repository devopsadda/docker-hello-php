# docker-hello-php
Build a docker image using a simple PHP Hello-World Application and run as a container (containerization php application)

## Step 01: Get Your application reay
```bash
mkdir docker-hello-world
cd docker-hello-world
mkdir src
cd src

vim index.php
```
```php
<?php

echo "Hello World ...!!!<br/>";
echo "I have successfully containerized my php application!!!";

?>
```
