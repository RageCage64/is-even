# AWK

## Modulo
Contibuted by: [TimRots](https://github.com/TimRots)


```awk
#!/usr/bin/awk -f

BEGIN{
        se = (num%2);
        if (se == 0) {
            print(se)
        }
}
```
```shell
$ awk -v num=666 -f is-even.awk
0
```
