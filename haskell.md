# Haskell

## The functional way
Contibuted by: [LloydTao](https://github.com/LloydTao)

functional program eppic performance

```Haskell
-- ebin recursion method
isEven :: Int -> String
isEven 0 = "Even"
isEven 1 = "Odd"
isEven n = isEven (n-2)

main :: IO ()
main = do
    n <- readLn :: IO Int
    putStrLn $ isEven $ abs n
    
```
