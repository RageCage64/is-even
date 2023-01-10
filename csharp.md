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

  public bool Calculate() {
    return NumberToCheck % 2 == 0;
  }
}
```

## The Linq
Contributed by: [Nick Martin](https://github.com/nickmartin1ee7)

.

```cs

bool isEven = Determine
    .With(2)
    .IsEven();
    
static class Determine
{
    public static T With<T>(this T @this) => @this;
    public static bool IsEven(this int number) => (number & 1) == 0;
}
```
