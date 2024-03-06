// Guessing Game in Terminal
package main

import (
	"bufio"
	"fmt"
	"math/rand"
	"os"
	"strconv"
	"strings"
	"time"
)

var attempts int

//var s = 0

func main() {
	target := randNum(1, 100)
	fmt.Println("1 ile 100 arasında rastgele seçilen sayıyı bulmaya çalışın.")
	for {
		if attempts == 5 {
			fmt.Printf("Maalesef kazanamadınız. Doğru yanıt %d idi :(", target)
			break
		}
		for attempts = 0; attempts < 5; attempts++ {
			reader := bufio.NewReader(os.Stdin)
			input, err := reader.ReadString('\n')
			input = strings.TrimSpace(input)
			num, err := strconv.Atoi(input)
			if err != nil {
				fmt.Println("Sayıdan başka karakter kullanılmaz")
				attempts++
				break
			}
			if (num < 0) || (num > 100) {
				fmt.Println("1 ile 100 arasında bir değer giriniz. Lütfen tekrar deneyin:")
				attempts += 1
				break
			}
			if num > target {
				fmt.Println("Daha küçük bir sayı girerek tekrar deneyiniz :)")
				fmt.Println(5-attempts-1, "hakkınız kaldı.")
				continue
			} else if num < target {
				fmt.Println("Daha büyük bir sayı girerek tekrar deneyiniz :)")
				fmt.Println(5-attempts-1, "hakkınız kaldı.")
				continue
			} else {
				fmt.Printf("İşte bu! Doğru yanıt %d'idi %d seferde buldun.", target, attempts+1)
				//s += 1
				return
			}
			/*if s == 1 {
				return
			}*/
		}
	}
}
func randNum(min, max int) int {
	rand.Seed(time.Now().Unix())
	return rand.Intn(max-min) + min
}
