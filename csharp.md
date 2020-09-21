# C#

## The OOP
Contibuted by: [victormamede](https://github.com/victormamede)

The only way to do it if you're a master OOP programmer and know your patterns

```c#
class IsEven {
  public int NumberToCheck { get; private set; }

  public IsEven(int x) {
    NumberToCheck = x;
  }

  public bool calculate() {
    return NumberToCheck % 2 == 0;
  }
}
```
