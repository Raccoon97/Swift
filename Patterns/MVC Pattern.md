# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [MVC Pattern](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVC%20Pattern.md#mvc-pattern)
- [M - Model](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVC%20Pattern.md#m---model)
- [V - View](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVC%20Pattern.md#v---view)
- [C - Controller](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVC%20Pattern.md#c---controller)
- [MVC Pattern μ μμ](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVC%20Pattern.md#mvc-pattern-%EC%9D%98-%EC%98%88%EC%8B%9C)
- [MVC Pattern μ μ₯/λ¨μ ](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVC%20Pattern.md#mvc-pattern-%EC%9D%98-%EC%9E%A5%EB%8B%A8%EC%A0%90)

<br><br><br>

# MVC Pattern
- μννΈμ¨μ΄ λμμΈ ν¨ν΄ μ€ νλμ΄λ€.
- MVC Cocoa Pattern μ΄λ€.
- Application μ 3 κ°μ μμ­μΌλ‘ λΆν νκ³  κ° μμ­μ κ³ μ ν μ­ν μ λΆμ¬νλ λ°©μμ΄λ€.
- MVC Pattern μ λμνλ©΄ λΉμ¦λμ€ λ‘μ§ μμ­κ³Ό UI μμ­μ΄ λΆλ¦¬λλ―λ‘ μλ‘ μν₯μ μ£Όμ§ μκ³  μ μ§λ³΄μκ° κ°λ₯νλ€.
>- μλ¬΄μ νμν λ°μ΄ν° μ²λ¦¬λ₯Ό μννλ λ‘μ§
- UIKit μ μ¬μ©νλ μ±μ κ΅¬μ‘°λ MVC λμμΈ ν¨ν΄μ κΈ°λ°μΌλ‘ νλ€.

<br>

<p align="center">
  <img src="https://user-images.githubusercontent.com/101554627/167997796-34cb28da-ded7-4f4a-9334-ce0518c884a3.png" alt="center" />
</p>

<br><br><br>

# M - Model
- View μ κ·Ό : λΆκ°
- Controller μ κ·Ό : Notification & KVO λ°©μμ ν΅ν΄ λͺ¨λΈμ λ³νλ₯Ό Controller μκ² μλ¦΄ μ μλ€.
- Application μ λ°μ΄ν°μ λΉμ¦λμ€ λ‘μ§μ κ΄λ¦¬νλ€.
>- λ€νΈμν¬ μ½λ
>- νμ± μ½λ
>- κ΄λ¦¬μ λ° μΆμν κ³μΈ΅/ν΄λμ€
>- λ°μ΄ν° μμ€ λ° delegates
>- μμ

<br><br><br>

# V - View
- Model μ κ·Ό : λΆκ°
- Controller μ κ·Ό : target - action κ΅¬μ‘°λ‘ μ¬μ©μμ νμμ λ°λΌ νμν ν¨μλ₯Ό νΈμΆν  μ μμΌλ©°, κ΅¬μ‘°μ μΌλ‘ λ―Έλ¦¬ μ ν΄μ§ λ°©μμΌλ‘ νμμ λν μμ²­(delegate), λ°μ΄ν°μ λν μμ²­(data-source) μ ν  μ μλ€.
- λ°μ΄ν°λ₯Ό μκ°μ μΌλ‘ νννλ€.
- λΉμ¦λμ€ λ‘μ§μ΄ ν¬ν¨λμ΄μμ§ μκΈ° λλ¬Έμ μ¬μ¬μ©μ΄ κ°λ₯ν κ²½μ°κ° λ§λ€.
- View λ μ΄μ΄μ κ²μ¬
>- Model λ μ΄μ΄μ μνΈμμ© νλμ§?
>- λΉμ¦λμ€ λ‘μ§μ΄ ν¬ν¨λμ΄ μλμ§?
>- UIμ κ΄λ ¨μ΄ μλ μμμ νλ €κ³  νλμ§?
- μ μΈκ°μ§ μ§λ¬Έ μ€ νλλΌλ κΈμ μ΄λ©΄ λ¦¬νν λ§μ ν΄μΌνλ€.

<br><br><br>

# C - Controller
- Model μ κ·Ό : κ°λ₯
- View μ κ·Ό : κ°λ₯
- Delegate Pattern μ ν΅ν΄ View μ Model μ¬μ΄λ₯Ό μ€μ¬νλ€.
- View μ Model μ¬μ΄μμ μ μ νκ² λ°μ΄ν°λ₯Ό μ΄λνλ©° λΈλ¦Ώμ§ μ­ν μ νλ€.
- Application μμ κ°μ₯ μ¬μ¬μ©μ΄ μ μ λΆλΆμ΄λ€.
- λ€μκ³Ό κ°μ μν©μ κ²°μ νλ λ μ΄μ΄μ΄λ€
>- κ°μ₯ λ¨Όμ  μ‘μΈμ€ ν΄μΌ νλ κ²?
>- μΌλ§λ μμ£Ό μ±μ μλ‘κ³ μ³μΌ νλμ§?
>- μ±μ΄ λ°±κ·ΈλΌμ΄λλ‘ μ΄λνλ©΄ λ¬΄μμ μ λ¦¬ν΄μΌ νλμ§?
>- μ¬μ©μκ° μμ ν­νμ λ λ¬΄μμ ν΄μΌ νλμ§?

<br><br><br>

# MVC Pattern μ μμ
- κΈ°μ‘΄ μ½λ
```swift
// ViewController.swift

import UIKit

class ViewController: UIViewController {
  @IBOutlet weak var message: UILabel!
  @IBOutlet weak var emailTxtField: UITextField!
  @IBOutlet weak var passwdTxtField: UITextField!
  
  var user_Email: String
  var user_Passwd: String
  
  override func viewDidLoad() {
    super.viewDidLoad()
    message.isHidden = true
  }
  
  @IBAction func didPressLogin(_ sender: UIButton) {
    guard let email = emailTxtField.text else {return}
    guard let passwd = passwdTxtField.text else {return}
    
    user_Email = email
    user_Passwd = passwd
    
    if user_Email == "test@gmail.com" && user_Passwd == "12345" {
      message.text = "λ‘κ·ΈμΈ μ±κ³΅"
      message.text.isHidden = false
    }
  }
}
```

- MVC Pattern μΌλ‘ λ³κ²½ν μ½λ
```swift
// ViewController.swift --> View, Controller

import UIKit

// Controller
class ViewController: UIViewController {

  // View
  @IBOutlet weak var message: UILabel!
  @IBOutlet weak var emailTxtField: UITextField!
  @IBOutlet weak var passwdTxtField: UITextField!
  
  var user: User!
  
  override func viewDidLoad() {
    super.viewDidLoad()
    message.isHidden = true
  }
  
  @IBAction func didPressLogin(_ sender: UIButton) {
    guard let email = emailTxtField.text else {return}
    guard let passwd = passwdTxtField.text else {return}
    
    user = User(email: email, passwd: passwd
    
    if user.email == "test@gmail.com" && user.passwd == "12345" {
      message.text = "λ‘κ·ΈμΈ μ±κ³΅"
      message.text.isHidden = false
    }
  }
}
```
```swift
// User.swift --> Model
import Foundation

struct User {
  var email: String
  var passwd: String
}
```

<br><br><br>

# MVC Pattern μ μ₯/λ¨μ 
### μ₯μ 
- λ€λ₯Έ Pattern μ λΉν΄ μ½λλμ΄ λ§μ§ μλ€.
- Apple μμ κΈ°λ³Έμ μΌλ‘ μ§μνλ Pattern μ΄λ€.
- κ°λ° μλκ° λΉ λ₯΄κΈ° λλ¬Έμ μν€νμ²κ° μ€μνμ§ μμ λ, κ·λͺ¨κ° μμ νλ‘μ νΈμμ μ¬μ©νκΈ° μ’λ€.

### λ¨μ 
- View μ Controller κ° λλ¬΄ λ°μ νκ² μ°κ²°λμ΄ μλ€.
- Controller κ° View μ μλͺμ£ΌκΈ°κΉμ§ κ΄λκΈ° λλ¬Έμ View μ Controller λ₯Ό λΆλ¦¬νκΈ° μ΄λ ΅λ€.
>- μ¬μ¬μ©μ±μ΄ λ¨μ΄μ§κ³  μ λ νμ€νΈλ₯Ό μ§ννκΈ° μ΄λ ΅λ€.
- λλΆλΆμ μ½λκ° Controller μ λ°μ§λ  μ μλλ°, κ·Έλ° μ΄μ λ‘ MVCλ₯Ό Massive View Controller λΌκ³  λΆλ₯΄κΈ°λ νλ€.

<br><br><br>

# μ°Έμ‘°
- [κ°μ€νλ](https://junhyunny.github.io/information/design-pattern/mvc-pattern/)
- [Mozilla](https://developer.mozilla.org/ko/docs/Glossary/MVC)
- [sh9404λ](https://lsh424.tistory.com/44)
- [Heechanλ](https://medium.com/hcleedev/ios-%EA%B0%9C%EB%B0%9C-mvc-%ED%8C%A8%ED%84%B4%EA%B3%BC-uikit%EC%9D%98-viewcontroller-3fdb52f6b4b8)
- [Choi-Logλ](https://choi-log-life.tistory.com/entry/iOS-MVC-Pattern)
