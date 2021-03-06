# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [Extension](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Extension.md#extension)
- [Extension κ΅¬λ¬Έ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Extension.md#extension-%EA%B5%AC%EB%AC%B8)
- [μ°μ° νλ‘νΌν°](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Extension.md#%EC%97%B0%EC%82%B0-%ED%94%84%EB%A1%9C%ED%8D%BC%ED%8B%B0)
- [μ΄λμλΌμ΄μ ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Extension.md#%EC%9D%B4%EB%8B%88%EC%85%9C%EB%9D%BC%EC%9D%B4%EC%A0%80)
>- [ν΄λμ€μμμ μ΄λμλΌμ΄μ , λμ΄λμλΌμ΄μ ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Extension.md#%ED%81%B4%EB%9E%98%EC%8A%A4%EC%97%90%EC%84%9C%EC%9D%98-%EC%9D%B4%EB%8B%88%EC%85%9C%EB%9D%BC%EC%9D%B4%EC%A0%80-%EB%94%94%EC%9D%B4%EB%8B%88%EC%85%9C%EB%9D%BC%EC%9D%B4%EC%A0%80-extension)
>- [κ΅¬μ‘°μ²΄μμμ μ΄λμλΌμ΄μ ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Extension.md#%EA%B5%AC%EC%A1%B0%EC%B2%B4%EC%97%90%EC%84%9C%EC%9D%98-%EC%9D%B4%EB%8B%88%EC%85%9C%EB%9D%BC%EC%9D%B4%EC%A0%80)
- [Method](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Extension.md#method)
- [Mutating μΈμ€ν΄μ€ Method](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Extension.md#mutating-%EC%9D%B8%EC%8A%A4%ED%84%B4%EC%8A%A4-method)
- [μλΈμ€ν¬λ¦½νΈ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Extension.md#%EC%84%9C%EB%B8%8C%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8)
- [μ€μ²© νμ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Extension.md#%EC%A4%91%EC%B2%A9-%ED%83%80%EC%9E%85)


<br><br><br>

# Extension
- Extension μ κΈ°μ‘΄ Class, Struct, Enum, Protocol μ μλ‘μ΄ κΈ°λ₯( Property, Method, Initializer, Deinitializer ) μ μΆκ°νλ€.
- μλ³Έ μμ€μ μ κ·Όνμ§ λͺ»νλ νμλ€λ μλ‘μ΄ κΈ°λ₯μ λ§λ€ μ μλ€. ( μλ³Έ μμ€λ κ·Έλλ‘ λκ³  μνλ κΈ°λ₯λ§ μΆκ° )
- Extension μ Obj-C μ Category μ μ μ¬νλ€. ( μ΅λͺ Category )
- μ κΈ°λ₯μ μΆκ°ν  μ μμ§λ§ μ€λ²λΌμ΄λλ ν  μ μλ€.

<br><br><br>

# Extension κ΅¬λ¬Έ
```swift
extension SomeType {
  // new functionality to add to SomeType goes here
}
```
- Extension μ νλ μ΄μμ Protocol μ μ μ©ν  μ μλ€. 
- Protocol μ μΆκ°νλ €λ©΄ Class λλ Struct μμ λ€λ₯Έ Class λλ Struct λ₯Ό μ°Έμ‘°ν  λ μ²λΌ μ¬μ©νλ©΄ λλ€.

```swift
extension SomeType: SomeProtocol, AnotherProtocol {
  // implementation of protocol requirements goes here
}
```
- μλ‘ Extension μ μ μνλ©΄, κ±°κΈ°μ ν¬ν¨λ μ κΈ°λ₯λ€μ Extension μ μ μνκΈ° μ μ μμ±ν μΈμ€ν΄μ€λΌκ³  ν΄λ ν΄λΉ μ νμ λͺ¨λ  μΈμ€ν΄μ€μμ μ¬μ©ν  μ μλ€.

<br><br><br>

# μ°μ° νλ‘νΌν°
- Extension μ κΈ°μ‘΄ μ νμ Computed Property λ₯Ό μΆκ°ν  μ μλ€.
```swift
// μλ μμλ κ±°λ¦¬ λ¨μ μμμ λν 5κ°μ Computed Property μ Swfit μ Double ν΄λμ€μ Extension νλ€.
// μ¬κΈ°μ Double 1.0 μ 1m λ₯Ό λνλ΄λ κ²μΌλ‘ κ°μ£Όλλ€.
extension Double {
  var km: Double { return self * 1_000.0 }
  var m: Double { return self }
  var cm: Double { return self / 100.0 }
  var mm: Double { return self / 1_000.0 }
  var ft: Double { return self / 3.28084 }
}

let oneInch = 25.4.mm
 print(" One inch is \(oneInch) meters ") // "One inch is 0.0254 meters"
 
 let threeFeet = 3.ft
 print(" Three feet is \(threeFeet) meters ") // "Three feet is 0.914399970739201 meters "
```
- μ΄λ¬ν Computed Property λ Double κ°μ΄ νΉμ  κΈΈμ΄ λ¨μλ‘ κ°μ£Όλμ΄μΌ ν¨μ λνλΈλ€.
- λ°ν κ°μ Double μ νμ΄λ©° Double λ‘ κ°λ₯ν μνμ  κ³μ°μμ μ¬μ©ν  μ μλ€.
```swift
let aMarathon = 42.km + 195.m
print(" A marathon is \(aMaraton) meters long ") // "A marathon is 42195.0 meters long"
```
- Extension μ μλ‘μ΄ Computed Property λ₯Ό μΆκ°ν  μ μμ§λ§ Stored Property λ₯Ό μΆκ°ν  μ μμΌλ©° Property Observer λν μΆκ°λ  μ μλ€.
```swift
extension Int {
  var ten: Int = 10 // Extensions must not contain stored properties
}
```

<br><br><br>

# μ΄λμλΌμ΄μ 
### ν΄λμ€μμμ μ΄λμλΌμ΄μ , λμ΄λμλΌμ΄μ 
-  Designated initializer, deinitializer λ μΆκ°ν  μ μλ€.
-  Convenience initializer λ μΆκ°ν  μ μλ€. ( Convenience λ init μλ§ μ¬μ©ν  μ μμ )
-  Convenience initializer λ μ΅μ’μ μΌλ‘ Designated initializer λ₯Ό νΈμΆν΄μΌ νλ€.
```swift

// Designated
      // ν΄λμ€μ init Extension
      extension NSString {
        init { print("init") } 
      } // Error
        // Designated initializer cannot be declared in an extension of 'NSString'; did you mean this to be a convenience initializer?

      // ν΄λμ€μ deinit Extension
      extension NSString {
        deinit { print("deinit") } 
      } // Error
        // Deinitializers may only be declared within a class

// Convenience
    // ν΄λμ€μ convenience init Extension
    extension NSString {
      convenience init(name: NSString) {
        self.init()
    } // PASS

    // ν΄λμ€μ convenience deinit Extension
    extension NSString {
      convenience deinit(name: NSString) {
        self.deinit()
    } // Error
      // 'convenience' may only be used on 'init' declarations
      // Deinitalizers may only be declared within a class
```
### κ΅¬μ‘°μ²΄μμμ μ΄λμλΌμ΄μ 
- Extension μΌλ‘ μ΄λμλΌμ΄μ λ₯Ό μΆκ°ν  κ²½μ° Memberwise Initalizer( κΈ°λ³Έ μμ±μ ) λ₯Ό μ μ§ν μ± μλ‘μ΄ μ΄λμλΌμ΄μ λ₯Ό μΆκ°ν  μ μλ€.
- κ΅¬μ‘°μ²΄λ ν΄λμ€μ λ¬λ¦¬ μ΄λμλΌμ΄μ λ₯Ό λ°λ‘ κ΅¬ννμ§ μμμ κ²½μ°μ Memberwise λΌλ μ΄λμλΌμ΄μ λ₯Ό μλμΌλ‘ μ κ³΅νλ€.
- μ§μ  κ΅¬μ‘°μ²΄μ μ΄λμλΌμ΄μ λ₯Ό κ΅¬ννλ©΄ Memberwise Initializer λ μ κ³΅λμ§ μλλ€.
- κ΅¬μ‘°μ²΄μμλ Convenience ν€μλλ₯Ό μ¬μ©ν  μ μλ€.
- κ΅¬μ‘°μ²΄μμλ λμ΄λμλΌμ΄μ λ₯Ό μ¬μ©ν  μ μλ€.
```swift
struct test { }

  // κ΅¬μ‘°μ²΄μ init Extension
  extension test {
    init(value: Int { self.x = value } 
  } // PASS
```

<br><br><br>

# Method
- Extension μ μλ‘μ΄ Method λ₯Ό μΆκ°ν  μ μλ€.
- μλ μ½λλ μ Method λ₯Ό μΆκ°νλ μμμ΄λ€.
```swift
// μ΄ Method λ λ§€κ°λ³μκ° μκ³  κ°μ λ°ννμ§ μλ ν¨μμ΄λ€.
extension Int {
  func repetitions( task: () -> Void ) {
    for _ in 0..<self {
      task()
    }
  }
}

3.repetitions {
  print("Hello!")
}
// Hello!
// Hello!
// Hello!
```

<br><br><br>

# Mutating μΈμ€ν΄μ€ Method
- Extension μΌλ‘ μΆκ°λ Method λ μΈμ€ν΄μ€ μμ²΄λ₯Ό μμ ν  μλ μλ€.
- selfλ Immutating μ΄λ―λ‘ self λ₯Ό λ³κ²½ν΄μΌνλ Method λ mutating μ μ¬μ©ν΄μΌ νλ€.
- μλ μ½λλ μλ κ°μ μ κ³±νλ μλ‘μ΄ Method λ₯Ό μΆκ°νλ μμμ΄λ€.
```swift
extension Int {
  mutating func square() {
    self = self * self
  }
}
var someInt = 3
someInt.square() // 9
```

<br><br><br>

# μλΈμ€ν¬λ¦½νΈ
- Extension μ μ΄μ©ν΄ μ‘΄μ¬νλ νμμ μλ‘μ΄ Subscripts λ₯Ό μΆκ°ν  μ μλ€.
```swift
// subscript[n] μ μ«μμ μ€λ₯Έμͺ½μμλΆν° nλ²μ§Έ μμΉνλ μ μλ₯Ό λ°ννλ€.
extension Int {
    subscript(digitIndex: Int) -> Int {
        var decimalBase = 1
        for _ in 0..<digitIndex {
            decimalBase *= 10
        }
        return (self / decimalBase) % 10
    }
}
746381295[0] // 5
746381295[1] // 9
746381295[2] // 2
746381295[8] // 7

746381295[9] // 0, as if you had requested: 0746381295[9]
```

<br><br><br>

# μ€μ²© νμ
- Extension μ μ΄μ©ν΄ Class, Strucr, Enum μ μ€μ²© νμμ μΆκ°ν  μ μλ€.
- μλ μ½λλ Int μ μ€μ²©ν Enum μ μΆκ°νλ μμμ΄λ€.
```swift
// Kind λΌλ Enum μ, Int λ₯Ό μμ, 0, μμλ‘ νννλ€.
extension Int {
    enum Kind {
        case negative, zero, positive
    }
    var kind: Kind {
        switch self {
        case 0:
            return .zero
        case let x where x > 0:
            return .positive
        default:
            return .negative
        }
    }
}

// Kind νλ‘νΌν°λ₯Ό μ΄μ©ν΄ νΉμ  μκ° μμ, 0 μμ μΈμ§ λνλΈλ€.
func printIntegerKinds(_ numbers: [Int]) {
    for number in numbers {
        switch number.kind {
        case .negative:
            print("- ", terminator: "")
        case .zero:
            print("0 ", terminator: "")
        case .positive:
            print("+ ", terminator: "")
        }
    }
    print("")
}
printIntegerKinds([3, 19, -27, 0, -6, 0, 7]) // "+ + - 0 - 0 + "
```


<br><br><br>

μ°Έμ‘°
- [Swift Document](https://docs.swift.org/swift-book/LanguageGuide/Extensions.html)
