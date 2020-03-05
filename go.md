# Go

## No generics
Contibuted by: [Jan](https://github.com/eisenwinter)

```golang
package main

import "fmt"

func isEven(n int) bool {
	return n&1 == 0
}

func concurrentIsEvenEmitter(channel chan int) {
	for {
		in, ok := <-channel
		if !ok {
			fmt.Println("No.")
		}
		fmt.Printf("%d is even: %t\r\n", in, isEven(in))
	}
}

func main() {
	channel := make(chan int)
	go concurrentIsEvenEmitter(channel)
	for i := 0; i < 100; i++ {
		channel <- i
	}
	close(channel)
}
```

