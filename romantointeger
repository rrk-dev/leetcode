package main

import(
    "fmt"
)


func romanToInt(s string) int {
	if len(s) < 1 || len(s) > 15 {
		return 0
	}

	romanMap := map[string]int{"I": 1, "V": 5, "X": 10, "L": 50, "C": 100, "D": 500, "M": 1000}
	chars := []rune(s)
	finalNumber := 0
	for i := 0; i < len(chars); i++ {

		if i < len(chars)-1 && romanMap[string(chars[i])] < romanMap[string(chars[i+1])] {
			
			finalNumber += (romanMap[string(chars[i+1])] - romanMap[string(chars[i])])
			i = i + 1
		} else {
			finalNumber += romanMap[string(chars[i])]
		}
	}
    
	return finalNumber
}
