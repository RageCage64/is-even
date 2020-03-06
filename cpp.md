# C++

## The short way
Contibuted by: [BraydonKains](https://github.com/BraydonKains)

This is the way everyone in the Programmer Nullposting group says is the best.

```cpp
bool isEven(int x) {
    return x % 2 == 0;
}
```

## The bitwise AND way
Contibuted by: [Jared0801](https://github.com/Jared0801)

This way is slightly more optimized (depending on the compiler) and almost as short, but possibly harder to read.

```cpp
bool isEven(int x) {
    return (x & 0x1) == 0;
}
```
