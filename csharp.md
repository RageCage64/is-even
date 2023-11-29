# C#

## The OOP<sup>2</sup>
Contributed by: [Gammer0909](https://github.com/gammer0909)

Yes, I know this is really a java thing, but we do this in C# too, but with XML documentation so it's "readable" now

```csharp
/// <summary>
/// Main Interfaces for the Abstract Factory Pattern
/// </summary>
interface IEven {
    bool IsEven(int n);
}

/// <summary>
/// Main Interfaces for the Abstract Factory Pattern
/// </summary>
interface IOdd {
    bool IsOdd(int n);
}

/// <summary>
/// Abstraction of an integer that we can extend to create even and odd numbers; unlike the int struct
/// </summary>
abstract class Number {
    int n;
}

/// <summary>
/// Factory class that returns a number based on whether it is even or odd
/// </summary>
class NumberFactory {
    public static Number GetNumber(int n) {
        if (n % 2 == 0) {
            return new EvenNumber(n);
        } else {
            return new OddNumber(n);
        }
    }
}

/// <summary>
/// Concrete implementation of an even number
/// </summary>
class EvenNumber : Number, IEven {
    public EvenNumber(int n) {
        this.n = n;
    }

    /// <summary>
    /// Checks if a given number, n, is even, but of course it's even, this is an EvenNumber.
    /// </summary>
    public bool IsEven(int n) {
        return true;
    }
}

/// <summary>
/// Concrete implementation of an odd number
/// </summary>
class OddNumber : Number, IOdd {
    public OddNumber(int n) {
        this.n = n;
    }

    /// <summary>
    /// Checks if a given number, n, is odd, but of course it's odd, this is an OddNumber.
    /// </summary>
    /// <param name="n">The number to check</param>
    public bool isOdd(int n) {
        return true;
    }
}

// Sample Usage:
class Program {
    public static void Main() {
        var numbers = new List<Number>();
        numbers.Add(NumberFactory.GetNumber(1));
        numbers.Add(NumberFactory.GetNumber(2));
        numbers.Add(NumberFactory.GetNumber(3));
        numbers.Add(NumberFactory.GetNumber(4));
        numbers.Add(NumberFactory.GetNumber(5));
        numbers.Add(NumberFactory.GetNumber(6));
        numbers.Add(NumberFactory.GetNumber(7));
        numbers.Add(NumberFactory.GetNumber(8));
        numbers.Add(NumberFactory.GetNumber(9));
        numbers.Add(NumberFactory.GetNumber(10));

        var evens = numbers.OfType<IEven>().Where(n => n.IsEven(n));
        var odds = numbers.OfType<IOdd>().Where(n => n.IsOdd(n));

        Console.WriteLine("Evens:");
        foreach (var even in evens) {
            Console.WriteLine(even);
        }

        Console.WriteLine("Odds:");
        foreach (var odd in odds) {
            Console.WriteLine(odd);
        }
    }
}
```


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

Everything that can be Linq will be Linq.

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
