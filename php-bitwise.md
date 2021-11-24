# PHP

## The function way with bitwise operator
Contributed by [Valentin Silvestre](https://github.com/vasilvestre)


```PHP
<?php declare(strict_types=1);
function isEven(int $x) {
    return !($x & 1);
}
?>
```
