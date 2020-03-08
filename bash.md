# Bash

## bash function
Contibuted by: [TimRots](https://github.com/TimRots)


```bash
$ isEven() {
    [[ "$(($1%2))" == "0" ]] && echo 0
}
$ isEven 4
0
```
