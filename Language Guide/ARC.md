# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [ARC( Automatic Reference Counting )](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#arc-automatic-reference-counting-)
- [ARC μλ λ°©μ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#arc-%EC%9E%91%EB%8F%99-%EB%B0%A9%EC%8B%9D)
- [ARC μλ λ°©μμ μ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#arc-%EC%9E%91%EB%8F%99-%EB%B0%A9%EC%8B%9D%EC%9D%98-%EC%98%88)
- [ν΄λμ€ μΈμ€ν΄μ€ κ°μ Strong Reference Cycle](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#%ED%81%B4%EB%9E%98%EC%8A%A4-%EC%9D%B8%EC%8A%A4%ED%84%B4%EC%8A%A4-%EA%B0%84%EC%9D%98-strong-reference-cycle)
- [ν΄λμ€ μΈμ€ν΄μ€ κ°μ Strong Reference Cycle ν΄κ²°](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#%ED%81%B4%EB%9E%98%EC%8A%A4-%EC%9D%B8%EC%8A%A4%ED%84%B4%EC%8A%A4-%EA%B0%84%EC%9D%98-strong-reference-cycle-%ED%95%B4%EA%B2%B0)
>- [Weak Reference](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#weak-reference)
>- [Unowned Reference](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#unowned-reference)
>- [Unowned Optional Reference](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#unowned-optional-reference)
>- [Unowned Reference μ μμμ μΌλ‘ λν ν΄μ  λ Optional Properties](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#unowned-reference-%EC%99%80-%EC%95%94%EC%8B%9C%EC%A0%81%EC%9C%BC%EB%A1%9C-%EB%9E%98%ED%95%91-%ED%95%B4%EC%A0%9C-%EB%90%9C-optional-properties)
- [Closure λ₯Ό μν Strong Reference Cycle](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#closure-%EB%A5%BC-%EC%9C%84%ED%95%9C-strong-reference-cycle)
- [Clousre μ λν Strong Reference Cycle ν΄κ²° - μμ± μ€.. 2022_04_29](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#clousre-%EC%97%90-%EB%8C%80%ED%95%9C-strong-reference-cycle-%ED%95%B4%EA%B2%B0)
>- [Capture List μ μ - μμ± μ ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#arc-automatic-reference-counting-)
>- [Closure μ λν Weak Reference λ° Unowned Reference - μμ± μ€](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/ARC.md#arc-automatic-reference-counting-)





<br><br><br>
# ARC( Automatic Reference Counting )
- Swift λ ARC λ₯Ό μ¬μ©νμ¬ μ±μ λ©λͺ¨λ¦¬ μ¬μ©λμ μΆμ νκ³  κ΄λ¦¬νλ€.
- λλΆλΆμ κ²½μ° μλμΌλ‘ λ©λͺ¨λ¦¬ κ΄λ¦¬κ° μ΄λ£¨μ΄μ§λ©°, ARC λ ν΄λΉ μΈμ€ν΄μ€κ° λ μ΄μ νμνμ§ μμ λ λ©λͺ¨λ¦¬λ₯Ό μλμΌλ‘ ν΄μ νλ€.
>- Reference Counting μ class μΈμ€ν΄μ€μλ§ μ μ©λλ©°, struct λ° enum μ Reference Type μ΄ μλ Value Type μ΄λ―λ‘ Reference μ μν΄ μ μ₯ λ° μ λ¬λμ§ μλλ€.
- μλ μ΄λ―Έμ§λ κΈ°μ‘΄ MRC( Manual Reference Counting ) μ μ¬μ©νμ¬ retain/ release μ½λλ₯Ό λ£μ΄μ€¬μ λμ ARC λ₯Ό μ¬μ©νμ λ μ½λ μμ°μ±μ μ°¨μ΄λ₯Ό λ³΄μ¬μ€λ€.
<p align="center">
  <img src="https://developer.apple.com/library/archive/releasenotes/ObjectiveC/RN-TransitioningToARC/Art/ARC_Illustration.jpg" alt="center" />
</p>

<br><br><br>
# ARC μλ λ°©μ
- μΈμ€ν΄μ€λ₯Ό μμ±ν  λ λ§λ€ ARC λ ν΄λΉ μΈμ€ν΄μ€μ λν μ λ³΄λ₯Ό μ μ₯νκΈ° μν΄ Heap μμ­μ λ©λͺ¨λ¦¬λ₯Ό ν λΉνλ€.
>- ν λΉλ λ©λͺ¨λ¦¬λ ν΄λΉ μΈμ€ν΄μ€μ κ΄λ ¨λ μμ± κ°κ³Ό μΈμ€ν΄μ€μ λν μ λ³΄λ₯Ό λ³΄μ νλ€.
- μΈμ€ν΄μ€κ° λ μ΄μ νμνμ§ μμ κ²½μ° ARC λ ν΄λΉ μΈμ€ν΄μ€μμ μ¬μ©νλ λ©λͺ¨λ¦¬λ₯Ό ν΄μ νλ€.
- μ¬μ©μ€μΈ μΈμ€ν΄μ€μ ν λΉμ ν΄μ νλ κ²½μ°, λ μ΄μ ν΄λΉ μΈμ€ν΄μ€μ Property μ μμΈμ€ νκ±°λ Method λ₯Ό νΈμΆν  μ μλ€.
- μ¬μ©μ€μΈ μΈμ€ν΄μ€κ° μ μ§λκΈ° μν΄ ARC λ νμ¬ κ° ν΄λμ€ μΈμ€ν΄μ€λ₯Ό μ°Έμ‘°νλ μμ±, μμ λ° λ³μμ μλ₯Ό μΆμ νλ€.
>- ν΄λΉ μΈμ€ν΄μ€μ λν νμ± μ°Έμ‘°κ° νλ μ΄μ μ‘΄μ¬νλ ν μΈμ€ν΄μ€λ₯Ό ν λΉ ν΄μ νμ§ μλλ€.
>- μμ±, μμ λλ λ³μμ μΈμ€ν΄μ€λ₯Ό ν λΉν  λλ§λ€ Strong Reference λ₯Ό λ§λλλ°, μ°Έμ‘°κ° λ¨μ μλ ν ν λΉ ν΄μ λ₯Ό νμ©νμ§ μμ "κ°λ ₯ν μ°Έμ‘°" λΌκ³  νλ€.

<br><br><br>
# ARC μλ λ°©μμ μ
- μλ μμ λ Person ν΄λμ€λ₯Ό λ©λͺ¨λ¦¬μ ν λΉνκ³  name νλ‘νΌν°λ₯Ό μ¬μ©νλ©°, ν λΉλ μΈμ€ν΄μ€λ₯Ό λ©λͺ¨λ¦¬μμ ν΄μ νλ λ°©λ²μ λ³΄μ¬μ€λ€.
```swift
class Person {
    let name: String
    init(name: String) {
        self.name = name
        print("\(name) is being initialized")
    }
    deinit {
        print("\(name) is being deinitialized")
    }
}
```
- Person ν΄λμ€μλ μΈμ€ν΄μ€μ μμ±μμ, μΈμ€ν΄μ€μ μλ©Έμκ° μλ€.
- μμ±μμ μλ©Έμμλ λ©λͺ¨λ¦¬ ν λΉκ³Ό λ©λͺ¨λ¦¬ ν λΉ ν΄μ λ₯Ό κ°μμ μΌλ‘ νμΈν  μ μλ λ©μμ§κ° μΆλ ₯λλ€.
```swift
var reference1: Person?
var reference2: Person?
var reference3: Person?
```
- Person ν΄λμ€λ₯Ό μ°Έμ‘°νλ λ³μλ₯Ό μ μνλ€. Optional Type μ΄λ―λ‘ λ΄λΆ νλ‘νΌν°λ nil κ°μΌλ‘ μλ μ΄κΈ°ν λλ€.
- λ―Έλ¦¬ μ μν΄λ λ³μμ Person μΈμ€ν΄μ€λ₯Ό ν λΉνλ€.
```swift
reference1 = Person(name: "Raccoon97")
// Prints "Raccoon97 is being initialized"
```
- μ΄λμλΌμ΄μ κ° νΈμΆλλ©΄μ λ©μμ§λ₯Ό μΆλ ₯νλ€. μ΄κΈ°νλ₯Ό νμΈν  μ μλ€.
- Person μΈμ€ν΄μ€κ° reference1 λ³μμ ν λΉλμκΈ° λλ¬Έμ reference1 λ³μμμ Person μΈμ€ν΄μ€μ λν Strong Reference κ° λ°μνλ€.
- νλ μ΄μμ Strong Reference κ° μκΈ° λλ¬Έμ ARC λ ν΄λΉ Person μΈμ€ν΄μ€λ₯Ό λ©λͺ¨λ¦¬μ ν λΉνκ³ , ν΄μ λμ§ μλλ‘ νλ€.
- λμΌν Person μΈμ€ν΄μ€λ₯Ό λλ¨Έμ§ λ κ°μ λ³μμ ν λΉνλ©΄ ν΄λΉ μΈμ€ν΄μ€μ λν λ κ°μ Strong Reference κ° λ°μνλ€.
```swift
reference2 = reference1
reference3 = reference1
```
- μ΄μ  Person μ΄λΌλ λ¨μΌ μΈμ€ν΄μ€μ λν΄ 3κ°μ Strong Reference κ° λ°μνλ€.
```swift
reference1 = nil
reference2 = nil
```
- λ κ°μ λ³μμ nil μ ν λΉνμ¬ μλμ μ°Έμ‘°λ₯Ό ν¬ν¨ν Strong Reference 2κ°λ₯Ό λκ² λλ©΄ νλμ Strong Reference κ° λ¨μμκΈ°μ Person μΈμ€ν΄μ€κ° ν λΉ ν΄μ λμ§ μλλ€.
```swift
reference3 = nil
// Prints "John Appleseed is being deinitialized"
```
- λ§μ§λ§ μΈ λ²μ§Έ λ³μμ nil μ ν λΉνμ¬ λ§μ§λ§ Strong Reference λ₯Ό λκ² λλ©΄ μ΄μ  Person μΈμ€ν΄μ€μ μ°κ²°λ Strong Reference λ νλλ μμΌλ―λ‘ λμ΄λμλΌμ΄μ κ° νΈμΆλλ©΄μ λ©μμ§κ° μΆλ ₯λλ€.

<br><br><br>
# ν΄λμ€ μΈμ€ν΄μ€ κ°μ Strong Reference Cycle
- λ κ° μ΄μμ ν΄λμ€ μΈμ€ν΄μ€λ₯Ό μ¬μ©ν΄ μλ‘μ λν Strong Reference λ₯Ό λ°μμμΌ κ° μΈμ€ν΄μ€κ° λ€λ₯Έ μΈμ€ν΄μ€λ₯Ό κ³μ μ μ§μν€λ κ²½μ°λ₯Ό Strong Reference Cycle μ΄λΌκ³  νλ©°, μΈμ€ν΄μ€μ Strong Reference κ° μμ΄μ§μ§ μλλ‘ μ½λλ₯Ό μμ±ν  μ μλ€.
- ν΄λμ€ κ°μ κ΄κ³ μ€ μΌλΆλ₯Ό Strong Reference κ° μλ Weak Reference, Unowned Reference λ‘ μ μνμ¬ Strong Reference Cycle λ₯Ό ν΄κ²°ν  μ μλ€.
>- [Resolving Strong Reference Cycles Between Class Instances](https://docs.swift.org/swift-book/LanguageGuide/AutomaticReferenceCounting.html#ID52)
- μλ μμ λ μ΄λ»κ² Strong Reference Cycle μ΄ λ°μνλμ§ λ³΄μ¬μ€λ€.
```swift
class Person {
    let name: String
    init(name: String) { self.name = name }
    var apartment: Apartment?
    deinit { print("\(name) is being deinitialized") }
}

class Apartment {
    let unit: String
    init(unit: String) { self.unit = unit }
    var tennant: Person?
    deinit { print("Apartment \(unit) is being deinitialized") }
}
```
- Person μΈμ€ν΄μ€μλ νμμ μΌλ‘ name, μ νμ μΌλ‘ apartment νλ‘νΌν°λ₯Ό.   Apartment μΈμ€ν΄μ€μλ νμμ μΌλ‘ unit, μ νμ μΌλ‘ tennant νλ‘νΌν°λ₯Ό κ°μ§λ€.
- λ μΈμ€ν΄μ€ λͺ¨λ λ©λͺ¨λ¦¬ ν λΉ ν΄μ λ₯Ό κ°μμ μΌλ‘ νμΈν  μ μλ λ©μμ§κ° μΆλ ₯λλ€.
```swift
var john: Person?
var unit4A: Apartment?
```
- Person, Apartment ν΄λμ€λ₯Ό μ°Έμ‘°νλ λ³μλ₯Ό μ μνλ€. Optional Type μ΄λ―λ‘ λ΄λΆ νλ‘νΌν°λ nil κ°μΌλ‘ μλ μ΄κΈ°ν λλ€.
- λ―Έλ¦¬ μ μν΄λ λ³μμ Person, Apartment μΈμ€ν΄μ€λ₯Ό ν λΉνλ€.
```swift
john = Person(name: "John Appleseed")
unit4A = Apartment(unit: "4A")
```
- μλ μ΄λ―Έμ§λ λ μΈμ€ν΄μ€λ₯Ό λ§λ€κ³  ν λΉν ν κ° λ³μμ μ΄λ ν Strong Reference κ° μλμ§ λ³΄μ¬μ€λ€.

<br>

![image](https://docs.swift.org/swift-book/_images/referenceCycle01_2x.png)
- μ΄μ  λ μΈμ€ν΄μ€λ₯Ό μλ‘ μ°κ²°ν  μ μλ€.
```swift
john!.apartment = unit4A
unit4A!.tennant = john
```
- μλ μ΄λ―Έμ§λ λ μΈμ€ν΄μ€λ₯Ό μ°κ²°ν ν Strong Reference μ λ³νλ₯Ό λ³΄μ¬μ€λ€.

<br>

![image](https://docs.swift.org/swift-book/_images/referenceCycle02_2x.png)
- μ΄λ κ² λλ©΄ λ μΈμ€ν΄μ€ μ¬μ΄μ Strong Reference Cycle μ΄ λ°μνλ€. 
>- Person μΈμ€ν΄μ€μ Apartment μΈμ€ν΄μ€μ λν Strong Reference κ°,  Apartment μΈμ€ν΄μ€μ Person μΈμ€ν΄μ€μ λν Strong Reference κ° λ°μνκ² λλ€.

```swift
john = nil
unit4A = nil
```
- λ λ³μλ₯Ό nil λ‘ ν λΉνμ λ λμ΄λμλΌμ΄μ κ° νΈμΆλμ§ μλλ€. ( λ©μμ§κ° μΆλ ₯λμ§ μμ )
- Strong Reference Cycle μ λ μΈμ€ν΄μ€κ° λ©λͺ¨λ¦¬μμ ν λΉ ν΄μ  λλ κ²μ λ°©μ§νμ¬ μ±μμ λ©λͺ¨λ¦¬ λμλ₯Ό μΌμΌν¨λ€.
- μλ μ΄λ―Έμ§λ λ λ³μλ₯Ό nil λ‘ ν λΉνμ λ Strong Reference κ° μ΄λ»κ² λ¨μμλμ§ λ³΄μ¬μ€λ€.

<br>

![image](https://docs.swift.org/swift-book/_images/referenceCycle03_2x.png)
- Person μΈμ€ν΄μ€μ Apartment μΈμ€ν΄μ€ κ°μ Strong Reference λ μ μ§λλ©° λμ μ μλ€.

<br><br><br>
# ν΄λμ€ μΈμ€ν΄μ€ κ°μ Strong Reference Cycle ν΄κ²°
- Swift λ Strong Reference Cycle μ ν΄κ²°νλ λ κ°μ§ λ°©λ²μ μ κ³΅νλ€
>- Weak Reference: ν μͺ½ μΈμ€ν΄μ€μ μλͺ μ£ΌκΈ°κ° λ μ§§μ κ²½μ° μ¬μ©νλ€.( λ¨Όμ  ν λΉ ν΄μ λ  κ°λ₯μ±μ΄ λμ μΈμ€ν΄μ€ )
>- Unowned Reference: ν μͺ½ μΈμ€ν΄μ€μ μλͺ μ£ΌκΈ°κ° κ°κ±°λ κΈ΄ κ²½μ° μ¬μ©νλ€.( λ λμ€μ ν λΉ ν΄μ λκ±°λ κ°μ΄ ν λΉ ν΄μ λ  κ°λ₯μ±μ΄ λμ μΈμ€ν΄μ€ )
- λ κ°μ§ λ°©λ²μ μ¬μ©νλ©΄ ν μΈμ€ν΄μ€κ° λ€λ₯Έ μΈμ€ν΄μ€λ₯Ό Strong Reference νμ§ μκ³ λ λ€λ₯Έ μΈμ€ν΄μ€λ₯Ό μ°Έμ‘°ν  μ μλ€.
- μ¦, Strong Reference Cycle μ΄ λ°μλμ§ μκ³ λ μΈμ€ν΄μ€κ° μλ‘λ₯Ό μ°Έμ‘°ν  μ μλ€.

<br><br>

## Weak Reference
- ARC κ° μ°Έμ‘°λ μΈμ€ν΄μ€λ₯Ό ν λΉ ν΄μ νλ κ²μ λ§μ§ μλλ€.
- Strong Reference Cycle μ΄ λλ κ²μ λ°©μ§νλ€.
- νλ‘νΌν°, λ³μ μ μΈ μ μμ weak ν€μλλ₯Ό λ°°μΉνλ€.
```swift
// μμ
weak var tennant: Person?
```
- μΈμ€ν΄μ€λ₯Ό Strong Reference νμ§ μκΈ° λλ¬Έμ ν΄λΉ μΈμ€ν΄μ€λ₯Ό μ°Έμ‘°νλ λμ ν λΉ ν΄μ λ  μ μλ€.
- ARC λ μ°Έμ‘°νλ μΈμ€ν΄μ€κ° ν λΉ ν΄μ λ  λ Weak Reference λ₯Ό nil λ‘ ν λΉνλ€.
- Weak Reference λ λ°νμμ κ°μ nil λ‘ λ³κ²½ν  μ μλλ‘ ν΄μΌ νλ―λ‘ ν­μ μμκ° μλ Optional Type μ var νμμΌλ‘ μ μΈλλ€.
- ARC κ° Weak Reference μ nil μ ν λΉν  λ Property Observer λ νΈμΆλμ§ μλλ€. 
>- Property Observer λ λ¬΄μμΈκ°.. [Zeddλ λΈλ‘κ·Έ](https://zeddios.tistory.com/247]
- μλμ μμλ μμ μμμ κ°μ§λ§, Apartment ν΄λμ€μ tennant νλ‘νΌν°κ° Weak Reference λ‘ μ μΈλλ€.
```swift
class Person {
    let name: String
    init(name: String) { self.name = name }
    var apartment: Apartment?
    deinit { print("\(name) is being deinitialized") }
}

class Apartment {
    let unit: String
    init(unit: String) { self.unit = unit }
    weak var tennant: Person?
    deinit { print("Apartment \(unit) is being deinitialized") }
}
```
- λ λ³μμ, μΈμ€ν΄μ€ ν λΉ, λ μΈμ€ν΄μ€ κ°μ μ°κ²°μ μμ μμμ λμΌνλ€.
```swift
var john: Person?
var unit4A: Apartment?

john = Person(name: "John Appleseed")
unit4A = Apartment(unit: "4A")

john!.apartment = unit4A
unit4A!.tennant = john
```
- μλ μ΄λ―Έμ§λ λ μΈμ€ν΄μ€λ₯Ό μ°κ²°ν Reference μ μνλ₯Ό λ³΄μ¬μ€λ€.

<br>

![image](https://docs.swift.org/swift-book/_images/weakReference01_2x.png)
- Person μΈμ€ν΄μ€μλ μ¬μ ν Apartment μΈμ€ν΄μ€μ λν Strong Reference κ° μλ€.
- Apartment μΈμ€ν΄μ€μλ Person μΈμ€ν΄μ€μ λν Weak Reference κ° μλ€.
- μ¦, Person μΈμ€ν΄μ€λ₯Ό κ°κ³  μλ john λ³μλ₯Ό nil λ‘ ν λΉνλ©΄ λ μ΄μ Strong Reference κ° μ‘΄μ¬νμ§ μκ² λλ€.
```swift
john = nil
// Prints "John Appleseed is being deinitialized"
```
- Person μΈμ€ν΄μ€μ λμ΄λμλΌμ΄μ κ° νΈμΆλλ©° λ©μμ§κ° μΆλ ₯λμκ³ , λ μ΄μ Strong Reference κ° μμΌλ―λ‘ Apartment μΈμ€ν΄μ€μ tennant μμ±μ΄ nil λ‘ λ°λκ² λλ€.
- μλ μ΄λ―Έμ§λ Person μΈμ€ν΄μ€λ₯Ό κ°λ john λ³μλ₯Ό nil λ‘ ν λΉν λ€ Reference μ λ³νλ₯Ό λ³΄μ¬μ€λ€.

<br>

![image](https://docs.swift.org/swift-book/_images/weakReference02_2x.png)
- μ΄μ  λ¨μμλ μ μΌν Strong Reference λ Apartment μΈμ€ν΄μ€λ₯Ό κ°κ³  μλ unit4A λ³μμ΄λ€.
```swift
unit4A = nil
// Prints "Apartment 4A is being deinitialized"
```
- Apartment μΈμ€ν΄μ€μ λμ΄λμλΌμ΄μ κ° νΈμΆλλ©° λ©μμ§κ° μΆλ ₯λμκ³ , λͺ¨λ  Strong Reference κ° μ¬λΌμ§κ² λμλ€.
- μλ μ΄λ―Έμ§λ Apartment μΈμ€ν΄μ€λ₯Ό κ°λ unit4A λ³μλ₯Ό nil λ‘ ν λΉν λ€ Reference μ λ³νλ₯Ό λ³΄μ¬μ€λ€.

<br>

![image](https://docs.swift.org/swift-book/_images/weakReference03_2x.png)
- λ€λ₯Έ μμ€νμμμ Weak Reference
>- Garbage Collector λ₯Ό μ¬μ©νλ μμ€ν μμλ weak ν¬μΈν°κ° κ°λ¨ν μΊμ± λ©μ»€λμ¦μ μννκΈ° μν΄ μ¬μ©λλ€. < Ex) Java, Python >
>- Garbage Collector κ° λμνλ©΄μ weak ν¬μΈν°λ Strong Reference κ° μλ κ°μ²΄μ ν λΉ ν΄μ λ₯Ό μννκΈ° μν΄ μ¬μ©λλ€.
- ARCλ₯Ό μ¬μ©νλ©΄ Strong Reference κ° μ κ±°λλ μ¦μ μΈμ€ν΄μ€μμ μ°Έμ‘°νλ Weak Reference κ°μ΄ ν λΉ ν΄μ λλ€.
- Strong Reference Cycle λ°©μ§ λͺ©μ μ΄ μλ Strong Reference κ° 0μΈ κ°μ ν λΉ ν΄μ λ₯Ό μν΄ Weak Reference λ₯Ό μ°λ κ²μ μ ν©νμ§ μλ€.

<br><br>

## Unowned Reference
- Weak Reference μ λ§μ°¬κ°μ§λ‘ μΈμ€ν΄μ€λ₯Ό Strong Reference νμ§ μλλ€.
- λ€λ₯Έ μΈμ€ν΄μ€μ μλͺ μ£ΌκΈ°κ° κ°κ±°λ λ κΈ΄ κ²½μ°μ Unowned Reference λ₯Ό μ¬μ©νλ€.
- νλ‘νΌν°, λ³μ μ μΈ μ μμ unowned ν€μλλ₯Ό λ°°μΉνλ€.
```swift
// μμ
unowned var tennant: Person?
```
- Weak Reference λ κ°μ΄ nil μ΄μ΄λ κ΄μ°?μ§λ§ Unowned Reference λ ν­μ κ°μ΄ μμ΄μΌ νλ€.
- ARC λ Unowned Reference μ κ°μ nil λ‘ μ€μ νμ§ μλλ€.
>- ν­μ ν λΉ ν΄μ λμ§ μλλ€κ³  νμ νλ μΈμ€ν΄μ€μλ§ Unowned Reference λ₯Ό μ¬μ©νλ€.
>- μΈμ€ν΄μ€κ° ν λΉ ν΄μ λ ν Unowned Reference κ°μ μμΈμ€ νκ² λλ©΄ λ°νμ μ€λ₯κ° λ°μνλ€.
- μλ μμλ μμ νκ² Unowned Reference λ₯Ό μ¬μ©νλ λ°©λ²μ λ³΄μ¬μ€λ€.
- Customer, CreditCard λΌλ λ κ°μ ν΄λμ€λ₯Ό μ μνλλ° CreditCard ν΄λμ€λ ν­μ Customer μ μ°κ²°λλ©° CreditCard μΈμ€ν΄μ€λ Unowned Reference λ₯Ό ν΅ν΄ μΈμ λ μ§ ν λΉ ν΄μ λ  μ μλ€.
- CreditCard μΈμ€ν΄μ€λ μ«μ κ°κ³Ό Customer μΈμ€ν΄μ€λ₯Ό μ΄λμλΌμ΄μ μ μ λ¬ ν΄μΌλ§ μμ±μ΄ κ°λ₯νλ€.
```swift
class Customer {
    let name: String
    var card: CreditCard?
    init(name: String) {
        self.name = name
    }
    deinit { print("\(name) is being deinitialized") }
}

class CreditCard {
    let number: UInt64
    unowned let customer: Customer
    init(number: UInt64, customer: Customer) {
        self.number = number
        self.customer = customer
    }
    deinit { print("Card #\(number) is being deinitialized") }
}
```
>- CreditCard ν΄λμ€μ numer νλ‘νΌν°λ 32λΉνΈ λ° 64λΉνΈ μμ€νμμ 16μλ¦¬μ μΉ΄λ λ²νΈλ₯Ό μ μ₯ν  μ μμ λ§νΌ Int κ° μλ UInt64 λ‘ μ μνλ€.
- Customer ν΄λμ€λ₯Ό μ¬μ©νκΈ° μν΄ λ³μλ₯Ό μ μΈνλ€.
```swift
var john
```
- Customer μΈμ€ν΄μ€λ₯Ό λ§λ€κ³  card νλ‘νΌν°μ CreditCard μΈμ€ν΄μ€λ₯Ό ν λΉνλ€.
```swift
john = Customer(name: "John Appleseed")
john!.card = CreditCard(number: 1234_5678_9012_3456, customer: john!)
```
- μλ μ΄λ―Έμ§λ λ μΈμ€ν΄μ€λ₯Ό μ°κ²°νμ λ Reference μν©μ λ³΄μ¬μ€λ€.
<br>

![image](https://docs.swift.org/swift-book/_images/unownedReference01_2x.png)
- Customer μΈμ€ν΄μ€μ CreditCard μΈμ€ν΄μ€μ λν Strong Reference κ° μλ€.
- CreditCard μΈμ€ν΄μ€μ Customer μΈμ€ν΄μ€μ λν Unowned Reference κ° μλ€.
- Unowned Reference λλ¬Έμ john λ³μμ nil μ ν λΉνλ©΄ λμ΄μ Strong Reference κ° μκ² λλ€.

```swift
john = nil
// Prints "John Appleseed is being deinitialized"
// Prints "Card #1234567890123456 is being deinitialized"
```
- Customer μΈμ€ν΄μ€μ λμ΄μ Strong Reference κ° μκΈ° λλ¬Έμ ν λΉμ΄ ν΄μ λλ€.
- CreditCard μΈμ€ν΄μ€λ₯Ό μ΄μ΄μ£Όλ Customer μ Strong Reference κ° μκΈ° λλ¬Έμ CreditCard μΈμ€ν΄μ€λ ν λΉμ΄ ν΄μ λλ€.
>- Swift λ μ±λ₯μμ μ΄μ λ‘ λ°νμ μμ κ²μ¬λ₯Ό λΉνμ±ν νλ κ²½μ° Unsafe Unowned Reference λ₯Ό μ κ³΅νλ€.
>- μ¬μ©μλ ν΄λΉ Unsafe Unowned Reference λ₯Ό μ κ²ν  μ±μμ κ°λλ€.
>- Unsafe Unowned Reference λ₯Ό μ¬μ©νμ¬ μ½λλ₯Ό μ§°μ λ, λ§μ½ Unowned Reference λ₯Ό μ¬μ©ν μΈμ€ν΄μ€κ° ν λΉμ΄ ν΄μ λ ν μμΈμ€νλ €κ³  νλ©΄ νλ‘κ·Έλ¨μ κ·Έ μΈμ€ν΄μ€κ° μλ λ©λͺ¨λ¦¬ μμΉμ μμΈμ€ νλ €κ³  νλλ° μ΄λ μμ νμ§ μμ μμμ΄λ€. 

<br><br>

## Unowned Optional Reference
- ν΄λμ€μ λν Optional Reference λ₯Ό unowned λ‘ νμν  μ μλ€.
- ARCμ κ΄μ μμ Unowned Reference μ Weak Reference λ λμΌν λ§₯λ½μμ μ¬μ©μ΄ κ°λ₯νλ€.
- λμΌν λ§₯λ½μμ μ¬μ©μ΄ κ°λ₯νμ§λ§ Unowned Reference λ₯Ό μ¬μ©ν  λλ ν­μ μ ν¨ν κ°μ²΄λ₯Ό Reference νκ±°λ nil μΈμ§ νμΈν΄μΌ νλ€.
- μλ μμλ Unowned Optional Reference μ μμμ΄λ€.
```swift
class Department {
    var name: String
    var courses: [Course]
    init(name: String) {
        self.name = name
        self.courses = []
    }
}

class Course {
    var name: String
    unowned var department: Department
    unowned var nextCourse: Course?
    init(name: String, in department: Department) {
        self.name = name
        self.department = department
        self.nextCourse = nil
    }
}
```
- Department ν΄λμ€μ Course ν΄λμ€κ° μμΌλ©° Course ν΄λμ€ λ΄λΆμλ Unowned Reference κ° 2κ°μ§ μλ€.
```swift
let department = Department(name: "Horticulture")

let intro = Course(name: "Survey of Plants", in: department)
let intermediate = Course(name: "Growing Common Herbs", in: department)
let advanced = Course(name: "Caring for Tropical Plants", in: department)

intro.nextCourse = intermediate
intermediate.nextCourse = advanced
department.courses = [intro, intermediate, advanced]
```
- μμ μ½λλ Department μΈμ€ν΄μ€ νλμ 3κ°μ Course μΈμ€ν΄μ€λ₯Ό μμ±νκ² λλ€.
- κ° Course μΈμ€ν΄μ€ λΌλ¦¬λ Unowned Optional Reference λ‘, Department μΈμ€ν΄μ€μ Course μΈμ€ν΄μ€ λΌλ¦¬λ Unowned Reference λ‘ μ°κ²°λμ΄μλ€.
- μλμ μ΄λ―Έμ§λ Reference λ₯Ό μκ°μ μΌλ‘ λνλΈλ€.
<br>

![image](https://docs.swift.org/swift-book/_images/unownedOptionalReference_2x.png)

- Unowned Optional Reference λ Strong Reference κ° μμΌλ©΄ ARCκ° ν λΉμ ν΄μ νκ² λλ€.
- ARC μμ Unowned Reference μ λμΌνκ² λμνλ€.
>- ν λΉ ν΄μ λμ§ μμ λ€λ₯Έ μΈμ€ν΄μ€λ₯Ό ν­μ Reference νλλ‘ ν΄μΌ νλ€. 
- Unowned Optional Reference λ nil μ΄ ν λΉλ  μ μλ€.

<br><br>

## Unowned Reference μ μμμ μΌλ‘ λν ν΄μ  λ Optional Properties
- μμ μ΄ν΄λ³Έ Weak Reference μ Unowned Reference μ μμλ Strong Reference κ° μ¬λΌμ ΈμΌ νλ μλλ¦¬μ€μ΄λ€.
- μλλ¦¬μ€ 1 : Person, Apartment μμ 
>- λ λ€ nil μΌ μ μλ μΈμ€ν΄μ€κ° μλ‘ Strong Reference Cycle λ₯Ό μ λ°ν  κ°λ₯μ±μ΄ μλ μν©
>>- Weak Reference λ‘ ν΄κ²°μ΄ κ°λ₯νλ€.
- μλλ¦¬μ€ 2 : Customer, CreditCard μμ 
>- nil μ΄ λ  μ μλ μΈμ€ν΄μ€μ nil μ΄ λ  μ μλ μΈμ€ν΄μ€ μ¬μ΄μ Strong Reference Cycle μ΄ λ°μλ  κ°λ₯μ±μ΄ μλ μν©
>>- Unowned Referece λ‘ ν΄κ²°μ΄ κ°λ₯νλ€.
- μλλ¦¬μ€ 3 : 
>- κ° μΈμ€ν΄μ€μ νλ‘νΌν°λ ν­μ κ°μ κ°μ ΈμΌ νλ©°, μ΄κΈ°νκ° μλ£λλ©΄ κ° μΈμ€ν΄μ€μ νλ‘νΌν°λ nil μ΄λ©΄ μλλ€.
>>- ν ν΄λμ€μ Unowned νλ‘νΌν°λ₯Ό λ€λ₯Έ ν΄λμ€μ μμμ μΌλ‘ λνλμ§ μμ Optional νλ‘νΌν°μ κ²°ν©μΌλ‘ ν΄κ²°μ΄ κ°λ₯νλ€. λ νλ‘νΌν° λͺ¨λ Optional Wrapping μμ΄ μ§μ  μμΈμ€ ν  μ μμΌλ©° Reference Cycle μ΄ λ°μνλ κ²μΌ νΌν  μ μλ€.

- μλ μμλ Country, City λ ν΄λμ€λ₯Ό μ μνλ©° κ°κ° ν΄λμ€λ λ€λ₯Έ ν΄λμ€μ μΈμ€ν΄μ€λ₯Ό νλ‘νΌν°λ‘ μ μ₯νλ€.
- λͺ¨λ  Country λ ν­μ City κ° μμ΄μΌ νλ©° λͺ¨λ  City λ ν­μ Country μ μν΄μΌ νλ€.
```swift
class Country {
    let name: String
    var capitalCity: City!
    init(name: String, capitalName: String) {
        self.name = name
        self.capitalCity = City(name: capitalName, country: self)
    }
}

class City {
    let name: String
    unowned let country: Country
    init(name: String, country: Country) {
        self.name = name
        self.country = country
    }
}
```

- City μ μ΄λμλΌμ΄μ λ Country μ΄λμλΌμ΄μ  λ΄μμ νΈμΆλλ€.
- μ΄λ κ² νλ©΄ Country μ΄λμλΌμ΄μ κ° νΈμΆλκΈ° μ κΉμ§ City μ΄λμλΌμ΄μ λ Country μ λ¬λ  μ μλ€.
- Country μ νλ‘νΌν°μΈ capitalCity λ€μ ! λ₯Ό λΆμ¬μ μμμ μΌλ‘ λνλμ§ μμ Optional νλ‘νΌν°λ‘ μ μΈνλ€.
- μ΄λ κ² νλ©΄ capitalCity μλ nil κ°μ΄ μμΌλ―λ‘ Country μ name, capitalName μ μ νλ μ¦μ Country μ μ΄λμλΌμ΄μ κ° νΈμΆλλ€.
- Strong Reference Cycle μ λ°μμν€μ§ μκ³ λ Country λ° City μΈμ€ν΄μ€λ₯Ό λ§λ€ μ μλ€.

```swift
var country = Country(name: "Canada", capitalName: "Ottawa")
print("\(country.name)'s capital city is called \(country.capitalCity.name)")
// Prints "Canada's capital city is called Ottawa"
```

<br><br><br>

# Closure λ₯Ό μν Strong Reference Cycle
- ν΄λμ€ μΈμ€ν΄μ€ νλ‘νΌν°μ Closure λ₯Ό ν λΉνκ³  ν΄λΉ Closure μ λ³Έλ¬Έμ΄ μΈμ€ν΄μ€λ₯Ό Capture νλ κ²½μ°μλ Strong Reference Cycle μ΄ λ°μν  μ μλ€.
- μ΄ Capture λ Closure κ° μΈμ€ν΄μ€μ self.property, self.method λ₯Ό Capture ν΄μ λ°μνλλ° self κ° Strong Reference Cycle μ λ°μμν¨λ€.
-  μ΄ Strong Reference Cycle μ Closure κ° Class μ κ°μ Reference μ νμ΄κΈ° λλ¬Έμ λ°μνλ€.
>- νλ‘νΌν°μ Closure λ₯Ό ν λΉνλ©΄ ν΄λΉ Closure μ λν Reference λ₯Ό ν λΉνλ κ²μ΄λ€.
- λ κ°μ Strong Reference Cycle μ΄ μλ‘λ₯Ό μ μ§νκ³  μλλ° μ΄λ²μ Class - Class κ° μλ Class - Closure μΈ κ²½μ°μ΄λ€.
- Swift λ Closure Capture List λΌλ μλ£¨μμ μ κ³΅νλ€.
- μλ μμλ Class - Closure κ° Strong Reference Cycle μ λ°μμ λ³΄μ¬μ€λ€.
```swift
class HTMLElement {

    let name: String
    let text: String?

    lazy var asHTML: () -> String = {
        if let text = self.text {
            return "<\(self.name)>\(text)</\(self.name)>"
        } else {
            return "<\(self.name) />"
        }
    }

    init(name: String, text: String? = nil) {
        self.name = name
        self.text = text
    }

    deinit {
        print("\(name) is being deinitialized")
    }

}

var paragraph: HTMLElement? = HTMLElement(name: "p", text: "hello, world")
print(paragraph!.asHTML())
// Prints "<p>hello, world</p>"
```
- HTMLElement Class λ HTMLElement μΈμ€ν΄μ€μ κΈ°λ³Έκ°μΌλ‘ μ¬μ©λλ Closure μ¬μ΄μ Strong Reference Cycle μ λ°μμν¨λ€.
- μλ μ΄λ―Έμ§λ λ°μλ Strong Reference Cycle μ λ³΄μ¬μ€λ€.

<br>

![image](https://docs.swift.org/swift-book/_images/closureReferenceCycle01_2x.png)
>- Clousre κ° μ¬λ¬ λ² Reference νλλΌλ μΈμ€ν΄μ€μ self μ λν Strong Reference λ νλλ§ Capture λλ€.
- paragraph λ³μλ₯Ό nil λ‘ ν λΉνκ³  Strong Reference λ₯Ό λλλ€ ν΄λ Closure μ HTMLElement μΈμ€ν΄μ€ μ¬μ΄μ Strong Reference Cycle μ μ¬λΌμ§μ§ μλλ€.
```swift
paragraph = nil
```
- HTMLElement μ λμ΄λμλΌμ΄μ  λ©μμ§λ μΆλ ₯λμ§ μμλ€.

<br><br><br>
# Clousre μ λν Strong Reference Cycle ν΄κ²°
- Clousre Capture List λ₯Ό μ μνμ¬ Closure μ Class μΈμ€ν΄μ€ κ°μ Strong Reference Cycle μ ν΄κ²°νλ€.
- Captue List λ Closure λ³Έλ¬Έ λ΄μμ νλ μ΄μμ Reference Type μ Capture ν  λ μ¬μ©ν  κ·μΉμ μ μνλ€.
- κ³μ..
