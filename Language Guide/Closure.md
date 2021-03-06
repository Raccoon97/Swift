# ๐    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   ๐ 
- [Closure](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Closure.md#closure)
- [Closure์ ํํ์](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Closure.md#closure%EC%9D%98-%ED%91%9C%ED%98%84%EC%8B%9D)
- [1๊ธ ๊ฐ์ฒด๋ก์์ Closure](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Closure.md#1%EA%B8%89-%EA%B0%9D%EC%B2%B4%EB%A1%9C%EC%84%9C%EC%9D%98-closure)
- [Closure ์คํํ๊ธฐ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Closure.md#closure-%EC%8B%A4%ED%96%89%ED%95%98%EA%B8%B0)
- [Closure ์ ๊ฒฝ๋ํ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Closure.md#closure-%EC%9D%98-%EA%B2%BD%EB%9F%89%ED%99%94)
- [Closure์ ๊ฒฝ๋ ๋ฌธ๋ฒ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Closure.md#closure%EC%9D%98-%EA%B2%BD%EB%9F%89-%EB%AC%B8%EB%B2%95)
- [@autoclosure](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Closure.md#autoclosure)
- [@escaping](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Closure.md#escaping)
- [Closure ์ Capture](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Closure.md#closure-%EC%9D%98-capture)
- [Closure ์ Capture List](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Closure.md#closure-%EC%9D%98-capture-list)
- [Closure ์ ARC( Automatic Reference Counting )](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Closure.md#closure-%EC%99%80-arc-automatic-reference-counting-)
- [Named Closure](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Closure.md#named-closure)



<br><br><br>



# Closure
- Named Closure
        - ํ์์ ์ผ๋ฐ์ ์ผ๋ก ์ฌ์ฉํ๋ ํจ์๋ Named Closure ์ด๋ค.
```swift
func doSomething() {
   print("Somaker")
}
```
- Unnamed Closure
        - ์ด๋ฆ์ ๋ถ์ด์ง ์๊ณ  ์ฌ์ฉํ๋ ํจ์๋ฅผ Unnamed Closure ๋ผ๊ณ  ํ๋ค.  
```swift
let closure = { print("Somaker") }
```
- ๋ณดํต Closure ํ๋ฉด Unamed Closure ๋ฅผ ์๋ฏธํ์ง๋ง ์ฌ์ค Named Closure ์ Unamed Closure ๋ ๋ค Closure ์ด๋ค.
- Closure ๋ ํจ์๋ผ์ " 1๊ธ ๊ฐ์ฒด ํจ์ " ์ ํน์ฑ์ ๋ค ๊ฐ๊ณ  ์๋ค.
- Closure ๋ ๋์, ๋ฐํ์ด ๊ฐ๋ฅํ๊ธฐ์ ์๋ฃํ์ ๊ฐ๊ณ  ์๋ค.
<br><br><br>
# Closure์ ํํ์

```swift
 {
     (Parameter) -> Return Type in         // Closure Head
     ์คํ ๊ตฌ๋ฌธ                               // Closure Body
 }
```
- ์ฃผ๋ก Closure ๋ฅผ ์ธ๊ธํ  ๋ ์ต๋ชํจ์( Unamed Closure ) ์ด๋ฏ๋ก func ํค์๋๋ ์ฌ์ฉํ์ง ์๋๋ค.
- Closure๋ Closure Head ์ Closure Body๋ก ์ด๋ฃจ์ด์ ธ ์๋๋ฐ, ๊ทธ ๋์ ๊ตฌ๋ถ์ง๋ ๊ฒ์ด in ํค์๋ ์ด๋ค.
- Parameter ์ Return Type ์ด ์๋ Closure
```swift
let closure = { () -> () in
   print("Closure")
}
```
>- Closure ๋ ์ต๋ชํจ์์ด๊ธด ํ์ง๋ง ํจ์์ด๋ค, ๋ฐ๋ผ์ Swift ์์ 1๊ธ ๊ฐ์ฒด ํจ์์ด๊ธฐ ๋๋ฌธ์, ์์์ ๋์์ด ๊ฐ๋ฅํ๋ค.
- Parameter ์ Return Type ์ด ์๋ Closure
```swift
let closure = { (name: String) -> String in
    return "Hello, \(name)"
}
```
>- ์ฌ๊ธฐ์ Parameter Name ์ Argument Name ์ด ์๋๋ค. Closure ๋ Argument Name ์ ์ฌ์ฉํ์ง ์๋๋ค.
- Ex
```swift
let closure = { (name: String) -> String in
    return "Hello, \(name)"
}

closure("Raccoon")
closure(name: "Raccoon")  //error!
```



<br><br><br>



# 1๊ธ ๊ฐ์ฒด๋ก์์ Closure
- Closure ๋ฅผ ๋ณ์๋ ์์์ ๋์ํ  ์ ์๋ค.
```swift
let closure = { () -> () in
    print("Closure")
}
```
>- ๋์๊ณผ ๋์์ Closure ๋ฅผ ์์ฑํ  ์ ์๋ค.
```swift
let closure2 = closure
```
>- ๊ธฐ์กด์ Closure ๋ฅผ ๋์ํ ๋ณ์๋ ์์๋ฅผ ์๋ก์ด ๋ณ์๋ ์์์ ๋์ํ  ์ ์๋ค.
- ํจ์์ ํ๋ผ๋ฏธํฐ ํ์์ผ๋ก Closure ๋ฅผ ์ ๋ฌํ  ์ ์๋ค.
```swift
func doSomething(closure: () -> ()) {
    closure()
}

doSomething(closure: { () -> () in
    print("Hello!")
})
```
>- ์ด์ฒ๋ผ ํจ์๋ฅผ ํ๋ผ๋ฏธํฐ๋ก ์ ๋ฌ๋ฐ๋ ํจ์๊ฐ ์๋ค, ํ์ง๋ง ํ๋ผ๋ฏธํฐ๋ฅผ Closure ๋ก ๋๊ฒจ์ค๋ ๋๋ค.
- ํจ์์ ๋ฐํ ํ์์ผ๋ก Closure ๋ฅผ ์ ๋ฌํ  ์ ์๋ค.
```swift
func doSomething() -> () -> () {
    return { () -> () in
        print("Hello!")
    }
}
```
>- ์ค์  Return์ ํ  ๋ ํจ์๊ฐ ์๋ Closure ๋ฅผ Returnํ  ์ ์๋ค.
```swfit
let closure = doSomething()
closure()
```
>- ๋ํ ์์์ ํจ์์ Return ๊ฐ( Closure )์ ๋์ํด์ ์์ ๊ฐ์ด ์คํํ  ์ ์๋ค.




<br><br><br>



# Closure ์คํํ๊ธฐ
- Closure ๊ฐ ๋์๋ ๋ณ์๋ ์์๋ก ํธ์ถํ๊ธฐ
```swift
let closure = { () -> String in
    return "Hello!"
}

closure()
```
>- ์ด์ฒ๋ผ ํด๋ก์ ๊ฐ ๋์๋ closure ์์๋ฅผ ํธ์ถ ๊ตฌ๋ฌธ์ธ () ๋ฅผ ์ด์ฉํด์ ์คํํ  ์ ์๋ค.
- Closure ๋ฅผ ์ง์  ํธ์ถํ๊ธฐ
```swift
({ () -> () in
    print("Hello!")
})()
```
>- ์ผํ์ฑ, ํด๋ก์ ๋ฅผ ์๊ดํธ๋ก ๊ฐ์ธ๊ณ  ๋์ ํธ์ถ ๊ตฌ๋ฌธ์ธ () ๋ฅผ ์ด์ฉํด์ ์คํํ  ์ ์๋ค.




<br><br><br>



# Closure ์ ๊ฒฝ๋ํ
- Trailling Closure
>- ํจ์์ ๋ง์ง๋ง Parameter๊ฐ Closure ์ผ ๋, ์ด๋ฅผ Parameter ํ์์ด ์๋ ํจ์ ๋ค์ ๋ถ์ฌ ์ฌ์ฉํ๋ ๋ฌธ๋ฒ, ์ด ๋, Argument Label ์ ์๋ต๋๋ค.
>>- Trailling Closure ๋ฅผ ์ฌ์ฉํ๊ธฐ ์ํ ์กฐ๊ฑด --> ๋ง์ง๋ง Parameter ๊ฐ Closure ์ผ ๊ฒฝ์ฐ
- Parameter ๊ฐ Closure ํ๋์ธ ํจ์
```swift
func doSomething(closure: () -> ()) {
    closure()
}
// ์ ํจ์๋ ์๋์ ๊ฐ์ด ํธ์ถ๋๋ค.

doSomething(closure: { () -> () in
    print("Hello!")
})
```
>- ์ด๋ ๊ฒ Closure ๊ฐ Parameter ํ์์ผ๋ก ํจ์์ ํธ์ถ ๊ตฌ๋ฌธ ์์ ์๋ ๊ฒ์ Inline Closure ๋ผ๊ณ  ๋ถ๋ฅธ๋ค.
>- ํจ์ ํด์์ด ์ฝ์ง๋ง์ ์์ ๋ชจ์์ ํจ์์ด๋ฏ๋ก ์ด ๋ ํจ์์ ๊ฐ์ฅ ๋ง์ง๋ง์ ๊ผฌ๋ฆฌ์ฒ๋ผ ๋ถ์ฌ ์ฌ์ฉํ  ์ ์๋ Trailling Closure ๋ฅผ ์ฌ์ฉํ๋ค.
```swift
// Trailling Closure
doSomething () { () -> () in
    print("Hello!")
}
```
>- Parameter ๊ฐ Closure ํ๋์ธ ๊ฒฝ์ฐ์๋ ๋ ๊ฒฝ๋ํ ์ํฌ ์ ์๋ค.( ํจ์ ํธ์ถ ๊ตฌ๋ฌธ์ธ () ๋ฅผ ์๋ต ๊ฐ๋ฅ )
```swift
doSomething () { () -> () in
    print("Hello!")
}
// ๊ธฐ์กด Trailling Closure ๋ฅผ ์ฌ์ฉํ์ ๋ ๋ชจ์ต

doSomething { () -> () in
    print("Hello!")
}
// Parameter ๊ฐ Closure ํ๋์ธ ๊ฒฝ์ฐ ๋ ๊ฒฝ๋ํ ๋ ๋ชจ์ต
```
- Parameter ๊ฐ ์ฌ๋ฌ ๊ฐ์ธ ํจ์
```swift
func fetchData(success: () -> (), fail: () -> ()) {
    //do something...
}
// ์ด๋ฐ ํจ์๊ฐ ์์ ๋ 

fetchData(success: { () -> () in
    print("Success!")
}, fail: { () -> () in
    print("Fail!")
})
// Inline Closure ์ ๊ฒฝ์ฐ


fetchData(success:  { () -> () in
    print("Success!")
}) { () -> () in
    print("Fail!")
}
// Trailling Closure ๋ฅผ ์ ์ฉํ ๋ชจ์ต, ๋ง์ง๋ง Parameter ๊ฐ Closure ์ด๊ธฐ์ Trailling Closure ๋ฅผ ์ฌ์ฉํ์ฌ ํํํจ
// ๋ง์ง๋ง Parameter ๋ง Argument Label ์ ์๋ตํ  ์ ์๋ค.
```



<br><br><br>



# Closure์ ๊ฒฝ๋ ๋ฌธ๋ฒ
- ๋ฌธ๋ฒ์ ์ต์ ํํ์ฌ Closure ๋ฅผ ๊ฐ๋จํ๊ฒ ์ธ ์ ์๋ ๊ฒ
```swift
func doSomething(closure: (Int, Int, Int) -> Int) {
    closure(1, 2, 3)
}
```
>- ๊ฒฝ๋ํ ํ  ํจ์ ์์

```swift
doSomething(closure: { (a: Int, b: Int, c: Int) -> Int in
    return a + b + c
})
```
>- Inline Closure ์์ฑ
- Parameter ํ์๊ณผ Return ํ์์ ์๋ตํ  ์ ์๋ค.
```swift
doSomething(closure: { (a, b, c ) in
    return a + b + c
})
```
>- Parameter ์๋ต, Return ์๋ต
- Parameter Name ์ Shortand Argument Names ๋ก ๋์ฒดํ๊ณ  ์ด ๊ฒฝ์ฐ Parameter Name ๊ณผ in ํค์๋๋ฅผ ์๋ตํ๋ค.
>- Shortand Argument Names ๋ a, b, c ๋ผ๋ Parameter Name ๋์ ์ $0, $1, $2 ์ ๊ฐ์ด $ ๊ณผ index ๋ฅผ ์ด์ฉํด์ Parameter ์ ์์๋๋ก ์ ๊ทผํ๋ ๊ฒ
```swift
doSomething(closure: {  
    return $0 + $1 + $2
})
```
>- Shortand Argument Names ๋ก Parameter ๋ฅผ ๋์ฒดํ์ฌ ๊ฒฝ๋ํ๋ Closure 
- ๋จ์ผ Return ๋ฌธ๋ง ๋จ์ ๊ฒฝ์ฐ Return ๋ ์๋ตํ  ์ ์๋ค, ๋จ์ผ Return ๋ฌธ์ด ์๋ ๊ฒฝ์ฐ์ Error๊ฐ ๋ฐ์ํ๋ค.
>- ๋จ์ผ Return ๋ฌธ์ด๋, Closure ๋ด๋ถ์ return ๊ตฌ๋ฌธ ํ๋๋ง ๋จ์ ์ํ 
```swift
doSomething(closure: {  
    $0 + $1 + $2
})
```
- Closure Parameter ๊ฐ ๋ง์ง๋ง Parameter ๋ผ๋ฉด Trailling Closure ๋ก ์์ฑํ๋ค.
```swift
doSomething() {  
     $0 + $1 + $2
}
```
>- Trailling Closure ๋ก ์์ฑํ์ฌ Closure ๋ฅผ ํจ์์ ๋ ๋ถ๋ถ์ผ๋ก ๋บ ๋ชจ์ต
- ํจ์ ํธ์ถ๋ถ์ ๋ณ๋ค๋ฅธ Argument ๊ฐ ์๋ค๋ฉด ()๋ฅผ ์๋ตํ  ์ ์๋ค.
```swift
doSomething { $0 + $1 + $2 }
```
>- Closure๋ฅผ ์ต์ข์ ์ผ๋ก ๊ฒฝ๋ํ ์ํจ ๋ชจ์ต



<br><br><br>



# @autoclosure
- ํ๋ผ๋ฏธํฐ๋ก ์ ๋ฌ๋ ์ผ๋ฐ ๊ตฌ๋ฌธ ๋๋ ํจ์๋ฅผ ํด๋ก์ ๋ก ๋ํ( Wrapping ) ํ๋ ๊ฒ
```swift
func doSomething(closure: @autoclosure () -> ()) {
}
```
>- ์ด๋ ๊ฒ autoclosure ๋ฅผ ์ฌ์ฉํ๊ฒ ๋๋ฉด ์ค์ ๋ก Closure ๋ฅผ ์ ๋ฌ๋ฐ์ง๋ ์์ง๋ง, Closure ์ฒ๋ผ ์ฌ์ฉ์ด ๊ฐ๋ฅํ๋ค.
>- ์ค์  Closure ์ ๋ค๋ฅธ ์ ์ ์ค์ ๋ก ์ ๋ฌํ๋ ๊ฒ์ด ์๋๊ธฐ ๋๋ฌธ์ ํ๋ผ๋ฏธํฐ๋ก ๊ฐ์ ๋๊ธฐ๋ ๊ฒ ์ฒ๋ผ ()๋ฅผ ํตํด ๋๊ฒจ์ค ์ ์๋ค.
```swift
func doSomething(closure: @autoclosure () -> ()) {
closure()
}

doSomething(closure: 1 > 2)
```
>- 1 > 2๋ Closure ๊ฐ ์๋ ์ผ๋ฐ ๊ตฌ๋ฌธ์ด์ง๋ง ์ค์  ํจ์ ๋ด์์๋ ์ผ๋ฐ ๊ตฌ๋ฌธ์ Closure ์ฒ๋ผ ์ฌ์ฉํ  ์ ์๋ค.
>- ํ์ง๋ง autoclosure ๋ฅผ ์ฌ์ฉํ  ๊ฒฝ์ฐ, ํ๋ผ๋ฏธํฐ๊ฐ ๋ฐ๋์ ์์ด์ผ ํ๋ค. ๋ฆฌํด ํ์์ ์๊ด ์๋ค.
- @autoclosure ํน์ง : ์ง์ฐ๋ ์คํ( Delayed Evaluation )
>- ์๋ ์ผ๋ฐ ๊ตฌ๋ฌธ์ด๋ผ๋ฉด ์์ฑ๋์๋ง์ ์คํ๋์ด์ผ ํ์ง๋ง autoclosure ๋ก ์์ฑํ ๊ตฌ๋ฌธ์ ํจ์๊ฐ ์คํ๋  ์์ ์ ๊ตฌ๋ฌธ์ Closure ๋ก ๋ง๋ค์ด ์ค์ผ๋ก ํจ์ ๋ด์์ ํด๋ก์ ๋ฅผ ์คํํ  ๋ ๊น์ง ๊ตฌ๋ฌธ์ด ์คํ๋์ง ์๋๋ค.
```swift
var names = ["Kim", "Park", "Lee"]

func doSomething(@autoclosure closure: () -> String) {
  closure()
}

names
// ["Kim", "Park", "Lee"]

doSomething(names.removeFirst())

names
// ["Park", "Lee"]
```
>- ์ง์ฐ๋ ์คํ์ autoclosure ๊ฐ ์๋ ์ผ๋ฐ Closure ๋ฅผ ์ฌ์ฉํ์ ๋๋ ์ ์ฉ๋๋ค.
```swift
var names = ["Kim", "Park", "Lee"]

let closure = {
  names.removeFirst()
}

names
// ["Kim", "Park", "Lee"]

closure()

names
// ["Park", "Lee"]
```
>- ์์ ๊ฐ์ด Closure ๋ฅผ ํธ์ถํ๊ธฐ ์ ๊น์ง๋ ์ ์ธ ๋จ๊ณ์์ ์์ฑ๋ ๊ตฌ๋ฌธ์ด ์คํ๋์ง ์๋๋ค.
>- ์ผ๋ฐ ๊ตฌ๋ฌธ์ autoclosure ๋ก ๋ํํ ๊ตฌ๋ฌธ์์ ์ง์ฐ๋ ์คํ์ด ๋ฐ์ํ๋ ์ด์ ์ด๋ค.
>- autoclosure ์์ฑ์ ๊ธฐ๋ณธ์ ์ผ๋ก @noescape ์์ฑ์ ๋ถ์ฌํ๋ค. ๊ทธ ์์ฑ์ ์์ ๊ธฐ ์ํด์๋ (escaping) ์ ์ด์ฉํ๋ค.
```swift
func doSomething(@autoclosure(escaping) closure: () -> String) {
  closure()
}
```



<br><br><br>



# @escaping
- ์ง๊ธ๊น์ง์ Closure ๋ ๋ชจ๋ non-escaping Closure ์ด๋ค, @escaping ํค์๋๊ฐ ์๋ Closure ๋ ๋ชจ๋ non-escaping Closure ์ด๋ค.
- non-escaping Closure ๋ ํจ์ ๋ด๋ถ์์๋ง ์ฐ์ด๊ธฐ ๋๋ฌธ์ ๋ฉ๋ชจ๋ฆฌ ๊ด๋ฆฌ๊ฐ ์ฉ์ดํด ์ฑ๋ฅ์ด ํฅ์๋๋ฉฐ ํจ์๊ฐ ์ข๋ฃ๋จ๊ณผ ๋์์ Closure ๋ ์ฌ์ฉ์ด ๋๋๋ค.
- escaping ์ ๊ฒฝ์ฐ, ํจ์๊ฐ ์ข๋ฃ๋๋๋ผ๋ ์ค์  Closure ๊ฐ ์ฌ์ฉ๋์ง ์์ ๋ ๊น์ง ๋ฉ๋ชจ๋ฆฌ๋ฅผ ์ถ์ ํด์ค์ผ ํ๋ค.
>- ํจ์ ๋ด๋ถ์์ ์ง์  ์คํํ๊ธฐ ์ํด์๋ง ์ฌ์ฉํ๋ค.
>- Parameter๋ก ๋ฐ์ Closure ๋ฅผ ๋ณ์๋ ์์์ ๋์ํ  ์ ์๋ค.
>>- ์ค์ ๋ก ๋ณ์๋ ์์์ Closure ๋ฅผ ๋์ํ๋ฉด, "Using non-escaping parameter 'closure' in a context expecting an @escaping closure" ๊ณผ ๊ฐ์ ์๋ฌ๊ฐ ๋ฐ์ํ๋ค.
>- ์ค์ฒฉ ํจ์์์ Closure ๋ฅผ ์ฌ์ฉํ  ๊ฒฝ์ฐ, ์ค์ฒฉ ํจ์๋ฅผ ๋ฆฌํดํ  ์ ์๋ค.
>- ํจ์์ ์คํ ํ๋ฆ ๋ฐ์ผ๋ก ๋๊ฐ ์ ์์ผ๋ฏ๋ก, ํจ์๊ฐ ์ข๋ฃ๋๊ธฐ ์ ์ ๋ฌด์กฐ๊ฑด ์คํ ๋์ด์ผ ํ๋ค.
>>- ํจ์๊ฐ ์ข๋ฃ๋๊ณ  ๋์ ํด๋ก์ ๊ฐ ์คํ๋  ์ ์๋ค.
```swift
func doSomething(closure: () -> ()) {
    let f: () -> () = closure // Using non-escaping parameter 'closure' in a context expecting an @escaping closure
}
// ํจ์๊ฐ ์ข๋ฃ๋๊ณ  ๋์ ํด๋ก์ ๊ฐ ์คํ๋  ์ ์๋ค๋ ์๋ฌ๊ฐ ๋ฐ์ํจ.
```

```swift
func doSomething(closure: () -> ()) {
    print("function start")
    
    DispatchQueue.main.asyncAfter(deadline: .now() + 10) { // Escaping closure captures non-escaping parameter 'closure'
        closure()
    }
    print("function end")
}
// ํจ์๊ฐ ๋๋๊ณ  ํด๋ก์ ๊ฐ ์คํ๋๊ธฐ ๋๋ฌธ์ ์๋ฌ๊ฐ ๋ฐ์ํจ.
```

```swift
func outer(closure: () -> ()) -> () -> () {
    func inner() {
        closure()
    }
    return inner // Escaping local function captures non-escaping parameter 'closure'
}
// ์ค์ฒฉ ํจ์ ๋ด๋ถ์์ ๋งค๊ฐ ๋ณ์๋ก ๋ฐ์ ํด๋ก์ ๋ฅผ ์ฌ์ฉํ  ๊ฒฝ์ฐ ์ค์ฒฉ ํจ์๋ฅผ ๋ฆฌํดํ  ์ ์๊ธฐ ๋๋ฌธ์ ์๋ฌ๊ฐ ๋ฐ์ํจ.
```
>- ์ ์๋ฌ์ ์์ธ์ non-escaping closure ์ ์ฃผ๋ณ ๊ฐ capture ๋ฐฉ์์ ์๋ค.
- ํจ์ ์คํ์ ๋ฒ์ด๋์ ํจ์๊ฐ ๋๋ ํ์๋ Closure ๋ฅผ ์คํํ๊ฑฐ๋, ์ค์ฒฉ ํจ์์์ ์คํ ํ ์ค์ฒฉ ํจ์๋ฅผ ๋ฆฌํดํ๊ณ  ์ถ๊ฑฐ๋, ๋ณ์๋ ์์์ ๋์ํ๊ณ  ์ถ์ ๊ฒฝ์ฐ์ @escaping ํค์๋๋ฅผ ์ฌ์ฉํ๋ค.
```swift
func doSomething(closure: @escaping () -> ()) {
}
// Closure Parameter ํ์ ์์ @escaping ์ ๋ถ์ฌ์ฃผ๋ฉด ๋๋ค.
```
- @escaping ํค์๋๋ฅผ ์ฌ์ฉํ  ๊ฒฝ์ฐ
>- ๋ณ์๋ ์์์ Parameter ๋ก ๋ฐ์ Closure ๋ฅผ ๋์ํ  ์ ์๋ค.
>- ํจ์๊ฐ ์ข๋ฃ๋ ํ์๋ Closure ๊ฐ ์คํ๋  ์ ์๋ค.
>- ์ค์ฒฉ ํจ์์์ ์คํ ํ ์ค์ฒฉ ํจ์๋ฅผ ๋ฆฌํดํ  ์ ์๋ค.



<br><br><br>



# Closure ์ Capture
- Closure ๋ ๋ด๋ถ ํจ์์ ๋ด๋ถ ํจ์์ ์ํฅ์ ๋ฏธ์น๋ ์ฃผ๋ณ ํ๊ฒฝ์ ๋ชจ๋ ํฌํจํ ๊ฐ์ฒด์ด๋ค.
```swift
func doSomething() {
    var message = "Hi i am sodeul!"
 
    //ํด๋ก์  ๋ฒ์ ์์
    
    var num = 10
    let closure = { print(num) }
 
    //ํด๋ก์  ๋ฒ์ ๋
    
    print(message)
}
// closure ๋ผ๋ ์ต๋ช ํจ์๋, Closure ๋ด๋ถ์์ ์ธ๋ถ ๋ณ์์ธ num ์ด๋ผ๋ ๋ณ์๋ฅผ ์ฌ์ฉํ๊ธฐ ๋๋ฌธ์ num ์ ๊ฐ์ Closure ๋ด๋ถ์ ์ผ๋ก ์ ์ฅํ๊ณ  ์๋ค.
// ์ด๊ฒ์ Closure ์ ์ํด num์ ๊ฐ์ด Capture ๋์๋ค ๋ผ๊ณ  ํ๋ค.
// message ๋ณ์๋ Closure ๋ด๋ถ์์ ์ฌ์ฉํ์ง ์๊ธฐ ๋๋ฌธ์ Closure ์ ์ํด ๊ฐ์ด Capture ๋์ง ์๋๋ค.
```
- Closure ์ ๊ฐ Capture ๋ฐฉ์
>- Closure ๋ ๊ฐ์ Capture ํ  ๋, Value/Reference ํ์์ ๊ด๊ณ ์์ด Reference Capture ํ๋ค.
>- ์ ์์์์ ์ดํด๋ณด๋ฉด num ์ Int ํ์์ ๊ตฌ์กฐ์ฒด ์ด๊ณ  ์ด๋ Value ํ์์ด๊ธฐ ๋๋ฌธ์, ๊ฐ์ ๋ณต์ฌํด์ ์ ์ฅํด์ผ ํ๋ค. ํ์ง๋ง Closure ๋ ํ์์ ๊ด๊ณ ์์ด Capture ํ๋ ๊ฐ๋ค์ Reference Capture ํ๋ค.

```swift
func doSomething() {
    var num: Int = 0
    print("num check #1 = \(num)")
    
    let closure = {
        print("num check #3 = \(num)")
    }
    
    num = 20
    print("num check #2 = \(num)")
    closure()
}
// --> num check #1 = 0
// --> num check #2 = 20
// --> num check #3 = 20

// Closure ๋ num ์ด๋ผ๋ ์ธ๋ถ ๋ณ์๋ฅผ Closure ๋ด๋ถ์์ ์ฌ์ฉํ๊ธฐ์ num ์ Capture ํ  ๊ฒ์ด๋ค.
// Closure ๋ฅผ ์คํํ๊ธฐ ์ ์ num ์ ๊ฐ์ ์ธ๋ถ์์ ๋ณ๊ฒฝํ๋ฉด Closure ๋ด๋ถ์์ ์ฌ์ฉํ๋ num ์ ๊ฐ ๋ํ ๋ณ๊ฒฝ๋๋ค.


func doSomething() {
    var num: Int = 0
    print("num check #1 = \(num)")
    
    let closure = {
        num = 20
        print("num check #3 = \(num)")
    }
    
    closure()
    print("num check #2 = \(num)")
}
// --> num check #1 = 0
// --> num check #3 = 20
// --> num check #2 = 20

// Closure ๋ด๋ถ์์ num ๊ฐ์ ๋ณ๊ฒฝํ๋ฉด Closure ์ธ๋ถ์ ์๋ num ์ ๊ฐ๋ ๋ณ๊ฒฝ๋๋ค.
```



<br><br><br>



# Closure ์ Capture List
- Closure ์ ์์์ธ { ์์ [ ] ๋ฅผ ์ด์ฉํ์ฌ Capture ํ  ๋ฉค๋ฒ๋ฅผ ๋์ดํ๋ค. in ํค์๋๋ ํจ๊ป ์์ฑํ๋ค.
```swift
let closure = { [num, num2] in ...
```
- Capture List ๋ฅผ ์ฌ์ฉํ๋ฉด Value ํ์์ ๊ฒฝ์ฐ Value Capture ๊ฐ ๊ฐ๋ฅํ๊ฒ ๋๋ค.
```swift
func doSomething() {
    var num: Int = 0
    print("num check #1 = \(num)")
    
    let closure = { [num] in
        print("num check #3 = \(num)")
    }
    
    num = 20
    print("num check #2 = \(num)")
    closure()
}
// --> num check #1 = 0
// --> num check #2 = 20
// --> num check #3 = 0
```
>- Value ํ์์ผ๋ก Capture ํ ๊ฒฝ์ฐ, Closure ๋ฅผ ์ ์ธํ  ๋น์์ num ์ ๊ฐ์ Const Value Type( ์์ ) ์ผ๋ก Capture ํ๋ค.
>- ๋ฐ๋ผ์ Closure ๋ด๋ถ์์ Value Capture ๋ ๊ฐ์ ๋ณ๊ฒฝํ  ์ ์๋ค.
```swift
let closure = { [num, num2] in
    num = 2 // Cannot assign to value: 'num' is an immutable capture
```
>- Closure ๋ ๊ธฐ๋ณธ์ ์ผ๋ก Value ํ์๋ Reference Capture ๋ฅผ ํ์ง๋ง, Closure Capture List ๋ฅผ ์ด์ฉํ๋ฉด Value Capture ๋ ๊ฐ๋ฅํ๋ค.
>- Reference ํ์์ ๊ฐ์ Closure Capture List ์ ์์ฑํ๋ค ํด๋ Value Capture ๊ฐ ๋์ง ์๊ณ  Reference Capture ๊ฐ ์ด๋ฃจ์ด์ง๋ค.
<br><br><br>
# Closure ์ ARC( Automatic Reference Counting )
- ARC
>- WWDC2021 ์์ ARC์ธ์ - https://developer.apple.com/videos/play/wwdc2021/10216/
>- ์ธ์คํด์ค์ Reference Count ๋ฅผ ์๋์ผ๋ก ๊ณ์ฐํ์ฌ ๋ฉ๋ชจ๋ฆฌ๋ฅผ ๊ด๋ฆฌํ๋ ๋ฐฉ๋ฒ.
>- ARC ๋ ๊ฐ์ฒด์ ๋ํ Reference Count ๋ฅผ ๊ด๋ฆฌํ๊ณ  0์ด ๋๋ฉด ์๋์ผ๋ก ๋ฉ๋ชจ๋ฆฌ ํด์ ํ๋ค.
>- Run Time ์ ๊ณ์ ์คํ๋๋ ๊ฒ ์๋๋ผ Compile Time ์ ์คํ๋๋ค.
>- Retain Cycle ์๋ ์ ์ํด์ผ ํ๋ค.
>>- Retain Cycle --> ๋ฉ๋ชจ๋ฆฌ๋ฅผ ์ฐจ์งํ๊ณ  ์๋ Reference ์ธ์คํด์ค๋ ์์ฃผ ๊ฐํ๊ฒ ์ฐ๊ฒฐ๋์ด ์๋ค.
>>- ์ธ์คํด์ค๋ค ๋ผ๋ฆฌ ๊ฐํ๊ฒ ์ฐ๊ฒฐ๋์ด ์๋ค๊ฐ nil ์ด ๋๋ฉด ๊ทธ ์๋ ํ๋กํผํฐ๋ผ๋ฆฌ ์ฐ๊ฒฐ๋ ๊ฒ๋ค์ ํด์ ๋์ง ์๊ณ  ๋จ์์๊ฒ ๋๋ฉฐ ๋ฉ๋ชจ๋ฆฌ ๋ฆญ์ ๋ฐ์์ํจ๋ค.
>>- ์ด๋ฐ ๋ฉ๋ชจ๋ฆฌ ๋ฆญ์ ๋ฐฉ์งํ๊ณ ์ ์ฐ๊ฒฐ์ํ๋ฅผ Strong, Weak, Unowned ์ผ๋ก ์ํฉ์ ๋ฐ๋ผ์ ๊ฒฐ์ ํ๋ ๊ฒ์ด Retain Cycle ์ด๋ค.
>- Obj-C ์์๋ MRC( Manual Reference Counting ), ์๋์ผ๋ก ๋ฉ๋ชจ๋ฆฌ๋ฅผ ๊ด๋ฆฌ ํ๋ค.
```obj-c
- (void)setName:(NSString *)newName {
  [newName retain];
  [name release];
  name = newName;
}
// retain : retain count( Reference Count ) ์ฆ๊ฐ๋ฅผ ํตํด ํ์ฌ Scope ์์ ๊ฐ์ฒด๊ฐ ์ ์ง๋๋ ๊ฒ์ ๋ณด์ฅ
// release : retain count( Reference Count ) ๋ฅผ ๊ฐ์์ํจ๋ค, retain ํ ํ์์์ด์ง ๋ release ํ๋ค.
```
>- ์๋์ ์ธ MRC ์๋ ๋ค๋ฅด๊ฒ ARC ๋ Compile Time ์ ์๋์ผ๋ก retain, release ๋ฅผ ์ ์ ํ ์์น์ ์ฝ์ํ๋ ๋ฐฉ์์ด๋ค.
>>- ๋์  ํ ๋น์ผ๋ก object ๊ฐ ์์ฑ๋๋ฉด ํด๋น ์ ๋ณด๋ HeapObject ๋ผ๋ struct ๋ก ๊ด๋ฆฌ๋๋ค.
>>- HeapObject ์์๋ Reference Count ๋ ํฌํจ๋๋ค.
>>- Class ์ ๋ํ HeapObject ๋ฅผ ํตํด Reference Count ๋ฅผ ๊ด๋ฆฌํ  ์ ์๋ค.
```swift
class Human {
    var name = ""
    lazy var getName: () -> String = {
        return self.name
    }
    
    init(name: String) {
        self.name = name
    }
 
    deinit {
        print("Human Deinit!")
    }
}
// Closure ๋ฅผ ํธ์ถ ์์๋ง ์ด๊ธฐํ ๋๊ฒ๋ lazy ํค์๋๋ฅผ ์ฌ์ฉํ๋ค.

var name: Human? = .init(name: "Hong-Gildong")
print(name!.getName())
// name ์ด๋ผ๋ ์ธ์คํด์ค๋ฅผ ๋ง๋ค๊ณ  Closure ๋ก ์์ฑ๋์ด ์๋ getName ์ด๋ ์ง์ฐ ์ ์ฅ ํ๋กํผํฐ๋ฅผ ํธ์ถํ๋ค.
// --> Hong-Gildong

name = nil

// name ์ธ์คํด์ค๊ฐ ํ์ ์์ด์ nil์ ํ ๋น์ ํ์ผ๋, ์ธ์คํด์ค์ Reference Count ๊ฐ 0์ด ๋์ด deinit ์ด ํธ์ถ๋์ด์ผ ํ๋ค.
// deinit ํจ์๊ฐ ํธ์ถ๋์ง ์์๋ค.
```
- Closure ์ ๊ฐํ ์ํ ์ฐธ์กฐ
>- Closure ๋ Reference ํ์์ผ๋ก Heap ์ ์กด์ฌํ๋ค.
>- ์ ์ฝ๋์์ ์์ฑํ human ์ด๋ผ๋ ์ธ์คํด์ค๋ getName ์ ํธ์ถํ๋ ์๊ฐ ๊ทธ Closure ๊ฐ Heap ์ ํ ๋น๋๋ฉฐ, ์ด Closure ๋ฅผ ์ฐธ์กฐํ๊ฒ ๋๋ค.
>- lazy ํค์๋๋ฅผ ์ฌ์ฉํ์ฌ ์ธ์คํด์ค ์์ฑ ์งํ๊ฐ ์๋, ํธ์ถ๋์ ์๊ฐ์ Heap ์ ํ ๋น๋๋ค.
>- getName ์ด๋ผ๋ Closure ๋ self ๋ฅผ ํตํด Human ์ธ์คํด์ค์ ํ๋กํผํฐ์ ์ ๊ทผํ๊ณ  ์์ผ๋ฉฐ, Closure ๋ ๊ฐ์ Capture ํ  ๋, Strong Capture๋ฅผ ํ๊ฒ ๋๋ค.
>- ๋ฐ๋ผ์ ์ด ๋ Human ์ธ์คํด์ค์ Reference Count ๊ฐ ์ฆ๊ฐํ๋ค.
>- * Human ์ธ์คํด์ค๋ Closure ๋ฅผ ์ฐธ์กฐํ๊ณ , Closure ๋ Human ์ธ์คํด์ค์ ๋ณ์๋ฅผ ์ฐธ์กฐํ๊ธฐ ๋๋ฌธ์ ๋ ๋ค ๋ฉ๋ชจ๋ฆฌ์์ ํค์ ๋์ง ์๋ ๊ฐํ ์ํ ์ฐธ์กฐ๊ฐ ๋ฐ์ํ๋ค.
>- ๊ฐํ ์ํ ์ฐธ์กฐ๋ weak, unowned ๋ฅผ ํตํด ํด๊ฒฐํ  ์ ์๋ค.
- Closure ์ ๊ฐํ ์ํ ์ฐธ์กฐ ํด๊ฒฐ๋ฒ
>- Closure ๊ฐ Property ์ ์ ๊ทผํ  ๋ self ๋ฅผ ์ฐธ์กฐํ๋ฉด์ ๋ฌธ์ ๊ฐ ๋ฐ์ํ๊ธฐ ๋๋ฌธ์ self ์ ๋ํ ์ฐธ์กฐ๋ฅผ Closure Capture List ๋ฅผ ์ด์ฉํด weak, unowned ๋ก Capture ํ๋ค.
```swift

class Human {
    lazy var getName: () -> String? = { [weak self] in
        return self?.name
    }
    
    init(name: String) {
        self.name = name
    }
 
    deinit {
        print("Human Deinit!")
    }
}
// weak ๋ฅผ ์ฌ์ฉํด์ Captureํ self 

class Human {
    lazy var getName: () -> String = { [unowned self] in
        return self.name
    }
    
    init(name: String) {
        self.name = name
    }
 
    deinit {
        print("Human Deinit!")
    }
}
// unowned ๋ฅผ ์ฌ์ฉํด์ Captureํ self 
```
>- ์ด๋ ๊ฒ ํ๋ฉด ์ธ์คํด์ค์ Reference Count ๊ฐ 0์ด ๋๋ฉด์ deinit ์ด ์ ์์ ์ผ๋ก ์ถ๋ ฅ๋๋ค.
>- weak ์ ๊ฒฝ์ฐ nil ์ ํ ๋น๋ฐ์ ๊ฐ๋ฅ์ฑ์ด ์๊ธฐ์ Optional Type ์ผ๋ก ์ฒ๋ฆฌํด์ค์ผ ํ์ง๋ง unowned ์ ๊ฒฝ์ฐ์ Non-Optional Type ์ผ๋ก ์ฌ์ฉํ  ์ ์๋ค.
>- Closure ๋ฅผ Lazy Initialization ์ผ๋ก ์ ์ธํ์ฌ ๊ฐํ ์ํ ์ฐธ์กฐ๊ฐ ์ผ์ด๋ ๊ฒฝ์ฐ, ์ธ์คํด์ค๊ฐ ์กด์ฌํด์ผ๋ง ์ด๊ธฐํ๊ฐ ๊ฐ๋ฅํ๊ณ , ์ด ๋๋ self ์ ๊ฐ์ด ์๋ค๊ณ  ๊ฐ์ ํ๊ธฐ ๋๋ฌธ์ unowned ๋ฅผ Optional Binding ์ ํ์ง ์๊ณ  ์ฌ์ฉํ  ์ ์๋ค.
>>- Swift 5.0 ๋ถํฐ๋ unowned ๋ Optional Type ์ด ๋์ง๋ง, Capture List ๋ก ๋์ํ  ๋ Non-Optional Type ์ด ๋๋ ๋ฏ ํ๋ค.



<br><br><br>




# Named Closure
- Named Closure ๋ ์ ์ญ ํจ์, ์ค์ฒฉ ํจ์ ๋ฅผ ๋ปํ๋ค.
>- ์ ์ญ ํจ์๋ ์ฃผ๋ณ์ ์ด๋ ํ ๊ฐ๋ Capture ํ์ง ์๋๋ค.
>- ์ค์ฒฉ ํจ์๋ ์์ ์ ํฌํจํ๊ณ  ์๋ ํจ์์ ๊ฐ์ Capture ํ๋ค.
```swift
func outer() {
    var num: Int = 0
    
    func inner() {
        print(num)
    }
}
```
>- ์ ์ฝ๋์์ inner() ๋ผ๋ ์ค์ฒฉ ํจ์๋ outer() ํจ์์ num ๊ฐ์ Reference Capture ํ๊ฒ ๋๋ค.



<br><br><br><br><br><br>




- ์ฐธ์กฐ
>- [์๋ค๋](https://babbab2.tistory.com/81?category=828998)
>- [์์ง๋](https://sujinnaljin.medium.com/ios-arc-%EB%BF%8C%EC%8B%9C%EA%B8%B0-9b3e5dc23814)
>- [Fomagran๋](https://fomaios.tistory.com/entry/iOS-%EB%A9%B4%EC%A0%91%EC%A7%88%EB%AC%B8-Retain-Cycle%EC%9D%B4%EB%9E%80?category=890971)
