Go (also called Golang) is a programming language Example
code`{{Code|1=package main

import "fmt"

func main() {
    fmt.Printf("Hello World!\n") // Prints hello world!
}|lang=go}}`{=mediawiki}

## Bitwise operators {#bitwise_operators}

  Operator                Description                              Example                  Explanation of example
  ----------------------- ---------------------------------------- ------------------------ ----------------------------------------------------------------------------------------------------------------
  \<\< (bitshift left)    Shifts binary left                       **10** \<\< **1** = 20   Moves the number 1 binary place left so 10 (00001010) changes to 20 (00010100), meaning it doubles the number.
  \>\> (bitshift right)   Shifts binary right                      **10** \>\> **1** = 5    Moves the number 1 binary place right so 10 (00001010) changes to 5 (00000101), meaning it halves the number.
  & (bitwise AND)         Keeps bit only if both numbers have it   60 & 13 = 12             60 (0011**11**00) and 13 (0000**11**01) both share the middle bits which means the result is 12 (0000**11**00)
  \| (bitwise OR)         Merges the binaries basically            60 \| 13 = 61            Keeps bit if either of them have it, 60 (00**1111**00) + 13 (0000**11**0**1**) = 61 (00**1111**0**1**)
  \^ (bitwise XOR)        Keeps only the differences               60 \^ 13 = 49            Keeps bit if both bits are different, 60 (00**1111**00) + 13 (0000**11**0**1**) = 49 (00**11**000**1**)

## Go standard library {#go_standard_library}

*Main article: [Go standard library](Go_standard_library "wikilink")*
