package main

import (
	"bufio"
	"fmt"
	"os"
	"strings"
)

func main() {
	reader := bufio.NewReader(os.Stdin)
	fmt.Println("Hi, I'm a basic chatbot. What's your name?")
	name, _ := reader.ReadString('\n')
	name = strings.TrimSpace(name)
	fmt.Printf("Nice to meet you, %s!\n", name)
	
	for {
		fmt.Print("You: ")
		input, _ := reader.ReadString('\n')
		input = strings.TrimSpace(input)

		if input == "exit" {
			fmt.Println("Goodbye!")
			break
		}

		response := getResponse(input)
		fmt.Println("Chatbot:", response)
	}
}

func getResponse(input string) string {
	
	return input
}
