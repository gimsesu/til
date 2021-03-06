# 빈 값 변수 선언

## 개요

- Go언어에서 자료구조 변수를 선언할 때, `nil` 값이 아닌 빈 자료구조 값으로 초기화 시켜야 할 때가 있다. 
-  `nil`값을 갖는 선언 방법은 대표적으로  `var` 선언문이 있다.
- 빈 자료구조를 만드는 가장 쉬운 방법으로는 `:=` 선언문이 있다.
- 이 글에서는 `:=`을 비롯하여 다양하게 빈 값을 갖는 자료구조 변수를 선언하는 방법을 알아본다.
- 💡자료형 변수는 `var`로 선언해도 `nil`값을 갖지 않는다.



## 예시

```go
///slice
var a []string  
if a == nil { 
    fmt.Println(true) 
} else { 
    fmt.Println(false) 
} 
// true
// nil 값으로 초기화된다.


b := []string{} 
if b == nil { 
    fmt.Println(true) 
} else { 
    fmt.Println(false) 
} 
// false
// 빈 슬라이스([]) 값으로 초기화된다.


c := make([]string, 0) 
if c == nil { 
    fmt.Println(true) 
} else { 
    fmt.Println(false) 
} 
// fasle
// 빈 슬라이스([]) 값으로 초기화된다.


var d []string = []string{} 
if d == nil { 
    fmt.Println(true) 
} else { 
    fmt.Println(false) 
}
// fasle
// 빈 슬라이스([]) 값으로 초기화된다.
```



## 📜참고

- [예제로 배우는 Go 프로그래밍 - Go 변수와 상수[Website]. (2020.11.18)](http://golang.site/go/article/4-Go-%EB%B3%80%EC%88%98%EC%99%80-%EC%83%81%EC%88%98)