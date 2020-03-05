# F#

## The short way
Contibuted by: [Jan](https://github.com/eisenwinter)

smol 1

```fsharp
let isEven x = 
  x &&& 1 = 0
```


big 1, cuz moar code = better

```fsharp
let isEven a =
    let isEven' a' =
      (fst a') = (abs a) || (snd a') = (abs a)
    seq { for i in 0..2..0x7FFFFFFF do yield (i, i+1) } 
    |> Seq.find isEven'
    |> fst |> abs = a
```