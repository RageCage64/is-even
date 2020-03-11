# Rust

## Non-Generic Remainder way
Contributed by: [daillen](https://github.com/daillen)

Simple stuff

```rust
fn is_even(x: i32) -> bool {
    (x % 2) == 0
}
```

## Generic Remainder way
Contributed by: [daillen](https://github.com/daillen)

Using generics and the remainder operator. Not so simple anymore...

```rust
use std::ops::Rem;

fn is_even<T: Rem<Output=T> + From<u8> + PartialEq>(x: T) -> bool {
    let rem = x % T::from(2);
    rem == T::from(0)
}
```

## Generic bit shift way
Contributed by: [daillen](https://github.com/daillen)

Using generics and the left and right bitshifts. ~~God help me~~

```rust
use std::ops::{Shl, Shr};

fn is_even<T: Copy + Shl<Output=T> + Shr<Output=T> + From<u8> + PartialEq>(x: T) -> bool {
    let one = T::from(1);
    x == (x >> one << one)
}
```
