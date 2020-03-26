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
