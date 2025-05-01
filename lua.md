# LUA

## The short way
Contributed by: [Dautomne_](https://github.com/FernandoNSC5)

This is the way everyone in the Programmer Nullposting group says is the best.

```lua
function isEven(num)
  return num % 2 == 0
end
```

## The OOP way
Contributed by: [daillen](https://github.com/daillen)

OOP is the best, right?

```lua
IsEven = {}

function IsEven:new(number)
  local obj = { number = number }
  setmetatable(obj, self)
  self.__index = self
  return obj
end

function IsEven:check()
  return self.number % 2 == 0
end

isEven = IsEven:new(10)
print(isEven:check())
```

## The time-arithmetic way
Contributed by: [fcr--](https://github.com/fcr--)

Converts `n*30` from a unix timestamp to a table where one of the fields is the
number of seconds.  Unixtime famously started at 1970-01-01 00:00:00,
so then `n*30` has 0 seconds if even or 30 seconds when odd.
```lua
function iseven(n)
   return os.date('!*t', n*30).sec == 0
end
```

## The syntax error way
Contributed by: [fcr--](https://github.com/fcr--)

Only an even number of consecutive backslashes are accepted in strings.

```lua
function iseven(n)
   return nil~=load('_="'..('\\'):rep(n)..'"')
end
```
