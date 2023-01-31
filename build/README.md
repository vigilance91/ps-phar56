# [vs\ps]()&trade;

# Copyright &copy; [Tyler R. Drury](https://vigilance91.github.io/) 19-07-2020, All Rights Reserved

## Proudly [Canadian](https://www.canada.ca/en.html), made in [Ontario](https://www.ontario.ca/)


---

**vs\ps.phar** is a PHP archive which contains Object oriented APIs for PHP resource types and global functions such as:

* (S)FTP connections
* IMAP connections
* CURL connections
* basic file and directory utilities
* openSSL operations
* logging and exception utilities


---

## License

vs_ps.phar is released under the modified Apache 2.0 License,
typical of all VS products.

See [LICENSE][7] file for details.

---

## Installing

### via composer
```
>composer require vs/ps
```
### via curl
```
>curl ftps://vs.ca/downloads/vs_ps.phar
```
### via github
```
>git ...
```

### Or simply

* visit the offical
[vs\ps&trade; PHAR](https://vs.ca/downloads/vs_ps.phar) site
* download the latest stable version via **FTPS**
[here](ftps://vs.ca/downloads/vs_ps.phar)
* clone the public github repository [here]()

Placing the .phar where desired in a project's directory structure

---

## Use

```php
//
require_once 'php/ps/meta.php';
//
use function ps/re/isAlpha as _isAlpha;
//
$a = isset($_GET('a')) and _isAlpha($_GET('a')) ? $_GET('a') : '';
//
//if $a does not have the format expected, kill execution
//
if($a === ''){
    //$a is unsafe, escape before output to browser
    $ea=htmlentities($a);
    die("invalid parameter $ea");
}
//
//$a is a string which is a single line and only contains a contiguous sequence of characters, without whitespace, numbers, punctuation or other special characters
//no worry about injection attacks if 'echo'ed back to a browser.
//also, important note, validation of a string using the regex engine is faster than performing entity escaping!
echo $a;
```

---

```
<?php
//include a local download of PHAR into a project
require_once "phar://" . LOCAL_PHAR_DIR . "/chrono.phar";
?>
```
or if using a locally installed version using composer,
included in the project's *composer.json* require,
simply use the composer supplied vendor's autload file
```
<?php
//include chrono.phar via composer supplied autoload file for this project
require_once dirname(__FILE__) . "/vendor/autoload.php";
?>
```

after which desire APIs may be used as follows

```
<?php
//
use \vs\chrono\Timer as Timer;
//
die(call_user_func(function(){
    $t = new Timer(false);
    $t->restart();
    //do stuff here
    $t->end();
    $delta = $t->getDelta();
    //
    echo "$delta" . PHP_EOL;
}));
```

---

## Authour, Owner and Primary Developer

* Tyler R. Drury


---

## Additional Contributors

* TBD


---

## Additional References and Resources

* The **official** [vs]() home site
* The **official** public [vs\chrono]() github repository
* The **official** [vs\chrono.phar]() library reference
* The **official** [vs\chrono_cli.phar]() CLI application reference


---
    
## Acknowledgments

* TBD

## Links


Authors and contributors are listed in the [AUTHORS.en.txt][8] file.

[1]: http://highlightjs.readthedocs.io/en/latest/api.html#inithighlightingonload
[2]: http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html
[3]: http://highlightjs.readthedocs.io/en/latest/api.html#highlightblock-block
[4]: http://highlightjs.readthedocs.io/en/latest/api.html#configure-options
[5]: https://highlightjs.org/download/
[6]: http://highlightjs.readthedocs.io/en/latest/building-testing.html
[7]: https://github.com/isagalaev/highlight.js/blob/master/LICENSE
[8]: https://github.com/isagalaev/highlight.js/blob/master/AUTHORS.en.txt
