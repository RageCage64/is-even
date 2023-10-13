# Java

## The "OOP is superior" way
Contrinuted by: [Gammer0909](https://github.com/Gammer0909)

The way you __have__ to do it at any java-based job, bloat is life!

```Java
class Number {
    int num;
}

interface IEven {
    public void isEven();
}

interface IFactory {
    public void getNumberObject();
}

class NumberFactory implements IFactory {
    public static Number getNumberObject() {
        Number n = new Number();
        return n;
    }
}

class Even extends Number implements IEven {
    Number n;

    Even(Number n) {
        this.n = n;
    }

    public void isEven() {
        if (n.num % 2 == 0) {
            System.out.println("Even");
        } else {
            System.out.println("Odd");
        }
    }
}

// Sample usage
class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        Number n = NumberFactory.getNumberObject();
        n.num = num;
        Even e = new Even(n);
        e.isEven();
    }
}
```

## The short way
Contributed by: [Ivan Jaramillo](https://github.com/IvanDavilaJaramillo)

This is the industrial way.

```Java
public class Even {
    public boolean isEven(int number) {
        return number % 2 == 0;
    }
}
```
