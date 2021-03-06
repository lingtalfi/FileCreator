FileCreator
================
2016-12-26 -> 2021-03-05



Create a file, line by line, or block by block.


FileCreator is part of the [universe framework](https://github.com/karayabin/universe-snapshot).


Install
=============


Using the [planet installer](https://github.com/lingtalfi/Light_PlanetInstaller) via [light-cli](https://github.com/lingtalfi/Light_Cli)
```bash
lt install Ling.FileCreator
```

Using the [uni tool](https://github.com/lingtalfi/universe-naive-importer)
```bash
uni import Ling/FileCreator
```



This class is very simple, and yet useful when you need to write some code, based
on conditions.

The available method are:

- line: creates one line
- block: creates a block of lines
- space: creates a space 


Example
============
```php


$c = new FileCreator();
$c->block('<?php
//--------------------------------------------
// FUNCTIONS
//--------------------------------------------
require_once __DIR__ . "/functions/main-functions.php";
');

$c->space(3);


$file = APP_ROOT_DIR . "/init.php";
if (false !== file_put_contents($file, $c->render())) {
    return true;
}
return false;


```
    
    


History Log
------------------

- 1.0.3 -- 2021-03-05

    - update README.md, add install alternative

- 1.0.2 -- 2020-12-08

    - Fix lpi-deps not using natsort.

- 1.0.1 -- 2020-12-04

    - Add lpi-deps.byml file

- 1.0.0 -- 2016-12-26

    - initial commit