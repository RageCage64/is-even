# sed

## String pattern
Contributed by: [fcr--](https://github.com/fcr--)

Check the last digit of the decimal representation:
```sed
s/^[0-9]*[02468]$/even/; t
s/.*/not even/
```

Test it by sending a number through the standard input:
```bash
$ echo 42 | sed -f iseven.sed
even
```

## Modulo 2
Contributed by: [fcr--](https://github.com/fcr--)

We calculate the remainder of the integer division by 2 for each digit, and then
discard all of them but the last one.
```sed
/^[0-9]\{1,\}$/!{ s/.*/not a number/; q }
y/0123456789/0101010101/
s/.*0/even/
s/.*1/odd/
```

```bash
$ echo 42 | sed -f iseven.sed
even
```
