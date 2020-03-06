# Javascript

## The short way
Contributed by: [BraydonKains](https://github.com/BraydonKains)

This is the way everyone in the Programmer Nullposting group says is the best.

```javascript
function isEven(x) {
    return x % 2 === 0;
}
```

## The fun way
Contributed by: [LeoCourbassier](https://github.com/LeoCourbassier)

Probably the worst way to check if a number is even. But hey, fun!

```javascript
class DiscreteIntegral {
  constructor(exp, intervals) {
    this.exponent = exp;
    this.intervals = intervals;
  }

  f(n) {
    let fApplied = Math.pow(n, this.exponent);
    if (!fApplied) return 0;

    return fApplied;
  }

  calculate(a, b) {
    let coefficient = (b - a) / this.intervals;
    let startingPoint = this.f(a) / 2;
    let endingPoint = this.f(b) / 2;
    let sum = 0;

    for (let i = 1; i <= this.intervals - 1; i++) {
      sum += this.f(a + (i * coefficient));
    }

    return coefficient * (startingPoint + sum + endingPoint);
  }
}

function isEven(n) {
  integral = new DiscreteIntegral(n, 100);
  let left = integral.calculate(-1, 0).toPrecision(5);
  let right = integral.calculate(0, 1).toPrecision(5);

  return left == right;
}
```
