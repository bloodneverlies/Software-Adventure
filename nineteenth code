// Guessing Game
package main

import (
	"fmt"
	"math/rand"
	"strconv"
	"time"

	"fyne.io/fyne/v2/app"
	"fyne.io/fyne/v2/container"
	"fyne.io/fyne/v2/widget"
)

var attempts1 int

func main() {
	rand.Seed(time.Now().Unix())
	target := randNum1(1, 100)

	myApp := app.New()
	myWindow := myApp.NewWindow("TAHMİN OYUNU")

	input := widget.NewEntry()
	input.SetPlaceHolder("TAHMİNİNİ GİR")
	output := widget.NewLabel("1 ile 100 arasında rastgele seçilen sayıyı bulmaya çalışın.")
	submit := widget.NewButton("DENE", func() {
		attempts1++
		guess, err := strconv.Atoi(input.Text)
		if err != nil || guess < 1 || guess > 100 {
			output.SetText("Geçersiz giriş. 1 ile 100 arasında bir sayı girin.")
			attempts1--
			return
		}
		if guess > target {
			output.SetText(fmt.Sprintf("Daha küçük bir sayı girerek tekrar deneyiniz :) %d hakkınız kaldı.", 7-attempts1))
		} else if guess < target {
			output.SetText(fmt.Sprintf("Daha büyük bir sayı girerek tekrar deneyiniz :) %d hakkınız kaldı.", 7-attempts1))
		} else {
			output.SetText(fmt.Sprintf("İşte bu! Doğru yanıt %d idi %d seferde buldun.", target, attempts1))
			return // Oyunu bitir
		}
		if attempts1 >= 7 {
			output.SetText(fmt.Sprintf("Maalesef kazanamadınız. Doğru yanıt %d idi :(", target))
		}
	})

	content := container.NewVBox(
		input,
		submit,
		output,
	)

	myWindow.SetContent(content)
	myWindow.ShowAndRun()
}

func randNum1(min, max int) int {
	return rand.Intn(max-min+1) + min
}
