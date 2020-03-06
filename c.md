# C

## The modulo way 
Contibuted by: [BraydonKains](https://github.com/BraydonKains)

This is the way everyone in the Programmer Nullposting group says is the best.

```c
int isEven(int x) {
    return x % 2 == 0;
}
```
## The bitshift way 
Contibuted by: [FeatherzMcCraw](https://github.com/FeatherzMcGraw)

Slide to the right... slide to the left...

```c
int isEven(int x) {
	return x == (x >> 1 << 1);
}
```

## The bitwise AND way
Contibuted by: [Jared0801](https://github.com/Jared0801)

This way is slightly more optimized (depending on the compiler) and almost as short, but possibly harder to read.

```c
int isEven(int x) {
    return (x & 0x1) == 0;