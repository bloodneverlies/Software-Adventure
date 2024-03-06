package main

import (
	"errors"
	"fmt"
)

func main() {
	result, err := evenNum(10)
	if err != nil {
		fmt.Println(err)
	} else {
		fmt.Println("The number is even and the entered number is :", result)
	}
}

func evenNum(num int) (int, error) {
	if num%2 != 0 {
		return 0, errors.New("incorrect input, this number is an even number")
	}
	return num, nil
}
