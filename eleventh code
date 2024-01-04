package main

import (
	"fmt"
)

func determinant3x3(matrix [3][3]int) int {
	result := 0

	result += matrix[0][0]*matrix[1][1]*matrix[2][2]
	result += matrix[0][1]*matrix[1][2]*matrix[2][0]
	result += matrix[0][2]*matrix[1][0]*matrix[2][1]
	result -= matrix[0][2]*matrix[1][1]*matrix[2][0]
	result -= matrix[0][0]*matrix[1][2]*matrix[2][1]
	result -= matrix[0][1]*matrix[1][0]*matrix[2][2]

	return result
}

func main() {
	var matrix [3][3]int

	fmt.Println("Enter 9 numbers for the 3x3 matrix:")

	for i := 0; i < 3; i++ {
		for j := 0; j < 3; j++ {
			fmt.Printf("Enter element at position [%d][%d]: ", i, j)
			_, err := fmt.Scan(&matrix[i][j])
			if err != nil {
				fmt.Println("Invalid input. Please enter a valid integer.")
				return
			}
		}
	}

	fmt.Println("\nEntered 3x3 Matrix:")
	for i := 0; i < 3; i++ {
		for j := 0; j < 3; j++ {
			fmt.Printf("%d\t", matrix[i][j])
		}
		fmt.Println()
	}

	det := determinant3x3(matrix)

	fmt.Printf("\nDeterminant of the Matrix: %d\n", det)
}
