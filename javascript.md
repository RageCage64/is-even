# Javascript

## The short way
Contibuted by: [BraydonKains](https://github.com/BraydonKains)

This is the way everyone in the Programmer Nullposting group says is the best.

```javascript
function isEven(x) {
    return x % 2 === 0;
}
```

## The bitwise AND way
Contibuted by: [Jared0801](https://github.com/Jared0801)

This way is slightly more optimized and almost as short, but possibly harder to read.

```javascript
function isEven(x) {
    if(x === undefined) return false;
    return (x & 0x1) === 0;
}
```

## The string conversion way
Contibuted by: [Jared0801](https://github.com/Jared0801)

This way isn't very optimal at all, but it makes sense I guess.

```javascript
function isEven(x) {
    return !(x/2).toString().includes('.');
}
```
