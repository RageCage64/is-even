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

## The "I'm a perl programmer" way
Contributed by [Alexander Wong](https://github.com/awwong1/)

Stringify and regex all of the things?

```python
import re

def is_even(x):
    return bool(re.search(r'[02468]$', str(x)))
```

## isEven API
Contributed by: [Tanner Collin](https://github.com/tannercollin)

Uses the [isEven API](https://isevenapi.xyz) free tier.

This tier only supports numbers 0 - 999,999. Upgrade to the Premium or Enterprise tier for more numbers.

```python
import requests

ISEVEN_API = 'https://api.isevenapi.xyz/api/iseven/'

def isEven(x):
    try:
        url = ISEVEN_API + str(x)
        r = requests.get(url, timeout=5)
        r.raise_for_status()
        return r.json()['iseven']
    except BaseException as e:
        print('isEven API problem:', e)
        return None
```
