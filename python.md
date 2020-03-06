# Python

## The short way
Contibuted by: [BraydonKains](https://github.com/BraydonKains)

This is the way everyone in the Programmer Nullposting group says is the best.

```python
def isEven(x):
    return x % 2 == 0
```
## The p y t h o n i c way
Contributed by: [Angus L'Herrou](https://github.com/angus-lherrou)

What, you aren't using generators? Are you even a python programmer?

```python
def is_even(x):
    return [even for n, even in zip(range(abs(x)+1), gen_even())][abs(x)]

def gen_even():
    even = True
    while True:
        yield even
        even = not even
```
