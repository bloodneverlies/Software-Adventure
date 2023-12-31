package main

import (
	"fmt"
	_ "fmt"
	_ "io/ioutil"
	"os"
)

func main() {
	path := "hny.txt"
	bs, err := os.ReadFile(path)
	if err != nil {
		fmt.Println("file not found")
		fmt.Println(err)
		return
	}
	str := string(bs)
	fmt.Println(str)
}
