# Brainfuck

[Brainfuck](https://esolangs.org/wiki/Brainfuck) is the most famous esoteric programming language.

## The basic algorithm
Contibuted by: [pufe](https://github.com/pufe)

Without comments
```brainfuck
,[>,]++++++[->++++++++<]<[[->>+<]>[<]<[->>-<]>[<]<]>>.

```

With comments
```brainfuck
,[>,] read until EOF
++++++[->++++++++<] sets answer to ASCII 0
< last char read
[ while not zero
[->>+<] if greater than zero then decrement once and increments answer
>[<]< returns to last char
[->>-<] if greater than zero then decrement once and decrements answer
>[<]< returns to last char
] end while
>>. prints answer
```
