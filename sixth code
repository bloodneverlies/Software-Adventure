package main

import (
	"fmt"
)

func main() {
	var examgrade int
	for {

		fmt.Println("enter your exam score:")
		_, err := fmt.Scan(&examgrade)
		if err != nil || examgrade < 0 || examgrade > 100 {
			fmt.Println("invalid data entry please enter a value between 0 and 100 inclusive.")
			continue
		}
		break
	}
	switch {
	case examgrade < 40:
		fmt.Printf("%d:terrible...", examgrade)
	case examgrade < 55:
		fmt.Printf("%d:bad...", examgrade)
	case examgrade < 70:
		fmt.Printf("%d:not bad...", examgrade)
	case examgrade < 85:
		fmt.Printf("%d:good...", examgrade)
	default:
		fmt.Printf("%d:awesome...", examgrade)
	}
}
