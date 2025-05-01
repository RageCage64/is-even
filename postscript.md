# PostScript

## The modulo way
Contributed by: [fcr--](https://github.com/fcr--)

```postscript
% Test it with eg: 42 iseven =
/iseven {2 mod 0 eq} bind def
```

## The bitwise way
Contributed by: [fcr--](https://github.com/fcr--)

```postscript
/iseven {1 and 0 eq} bind def
```

## The multiplicative {1, -1} group way
Contributed by: [fcr--](https://github.com/fcr--)

Given an integer $n$, we know that $(-1)^n$ is 1 when $n$ is even and -1 when it's odd.
This happens because $(-1)^{2m}=1^m=1$.
Here we use that property to check whether a number is even or not.

```postscript
/iseven {-1 exch exp 1 eq} bind def
```

