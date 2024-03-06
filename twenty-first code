package main
import (
	"bufio"
	"fmt"
	"os"
	"strconv"
	"strings"
)

func main() {
	fmt.Print("Lütfen aldığınız notu giriniz:")
	grade, err := getGrade()
	if err != nil {
		fmt.Println(err)
		return
	}
	var result string

	if grade >= 50 {
		result = "Geçtiniz"
	} else if grade >= 0 {
		result = "Kaldınz"
	}
	fmt.Println(result)
}

func getGrade() (int, error) {
	for {
		reader := bufio.NewReader(os.Stdin)
		input, err := reader.ReadString('\n')
		if err != nil {
			return 0, err
		}
		input = strings.TrimSpace(input)
		num, err := strconv.Atoi(input)
		if err != nil {
			fmt.Println("Not bir sayı olmalıdır")
			continue
		}
		if (num < 0) || (num > 100) {
			fmt.Println("Not 100 ile 0 arasında bir değer olmalıdır. Lütfen tekrar deneyin:")
			continue
		}
		return num, nil
	}
}
