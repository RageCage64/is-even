# PHP

## The function way
Contributed by [Eric Cheng](https://github.com/import-brain)


```PHP
<?php declare(strict_types=1);
function isEven(int $x) {
    if ($x % 2 == 0) {
        return true;
    } else {
        return false;
    }
}
?>
```
