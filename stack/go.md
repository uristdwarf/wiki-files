---
title: Go
description: 
published: true
date: 2022-08-07T14:37:34.706Z
tags: 
editor: markdown
dateCreated: 2022-08-04T16:21:17.702Z
---

# Go
Go (also called Golang) is a programming language

Example code
```go

import "fmt"

func main() {
    fmt.Printf("Hello World!\n") // Prints hello world!
}
```

## Bitwise operators {#bitwise_operators}
<table>
  <colgroup span="4"></colgroup>
  <tr>
    <th>Operator</th>
    <th>Description</th>
    <th>Example</th>
    <th>Explanation</th>
  </tr>
  
  <tr>
    <td><< (bitshift left) </td>
    <td>Shifts binary left </td>
    <td>10 << 1 = 20 </td>
    <td>Moves the number 1 binary place left so 10 (00001010) changes to 20 (00010100), meaning it doubles the number. </td>
  </tr>
  
  <tr>
    <td>>> (bitshift right) </td>
    <td>Shifts binary right</td>
    <td>10 >> 1 = 5 </td>
    <td>Moves the number 1 binary place right so 10 (00001010) changes to 5 (00000101), meaning it halves the number. </td>
  </tr>
    
  <tr>
    <td>& (bitwise AND) </td>
    <td>Keeps bit only if both numbers have it</td>
    <td>60 & 13 = 12 </td>
    <td>60 (00111100) and 13 (00001101) both share the middle bits which means the result is 12 (00001100) </td>
  </tr>
    
  <tr>
    <td>| (bitwise OR) </td>
    <td>Merges the binaries basically </td>
    <td>60 | 13 = 61 </td>
    <td>Keeps bit if either of them have it, 60 (00111100) + 13 (00001101) = 61 (00111101) </td>
  </tr>
    
  <tr>
    <td>^ (bitwise XOR) </td>
    <td>Keeps only the differences </td>
    <td>60 ^ 13 = 49 </td>
    <td>Keeps bit if both bits are different, 60 (00111100) + 13 (00001101) = 49 (00110001) </td>
  </tr>
</table>

## Go standard library {#go_standard_library}

*Main article: [Go standard library](go/library)*
