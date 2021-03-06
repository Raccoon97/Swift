# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [MVVM Pattern](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVVM%20Pattern.md#mvvm-pattern)
- [M - Model](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVVM%20Pattern.md#m---model)
- [V - View](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVVM%20Pattern.md#v---view)
- [VM - ViewModel](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVVM%20Pattern.md#vm---viewmodel)
- [Data Binding](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVVM%20Pattern.md#data-binding)
- [MVVM Pattern μμ](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVVM%20Pattern.md#mvvm-%EC%98%88%EC%8B%9C)
- [MVVM Pattern μ μ₯/λ¨μ ](https://github.com/Raccoon97/Swift/blob/main/Patterns/MVVM%20Pattern.md#mvvm-%EC%9D%98-%EC%9E%A5%EB%8B%A8%EC%A0%90)

<br><br><br>

# MVVM Pattern
- μννΈμ¨μ΄ λμμΈ ν¨ν΄ μ€ νλμ΄λ€.
- MVC  Pattern μμ Controller λ₯Ό λΉΌκ³  ViewModel μ μΆκ°ν Pattern μ΄λ€.
  - <p><h6>MVC Pattern μμλ λ€μν λ‘μ§μ Controller κ° μ²λ¦¬νκΈ° λλ¬Έμ Massive ν΄μ§λ λ¬Έμ κ° μλλ°, MVVM Pattern μμλ View μ μλ°μ΄νΈν  λ°μ΄ν°λ₯Ό View Model μμ μ²λ¦¬ν¨μΌλ‘μ¨ Controller κ° λ³΅μ‘ν΄μ§λ κ²μ μ€μ¬μ€λ€.</h6></p>

- MVVM μμλ View κ° ViewModel μ μμ νκ³ , ViewModel μ΄ Model μ μμ νλ λ°©μμ΄λ€.
- MVVM μ ν΅μ¬μ Data Binding μ΄λ€. 
  - <p><h6>Data Binding μ λ°μ΄ν°λ₯Ό μ κ³΅μΈ‘κ³Ό κ·Έ λ°μ΄ν°λ₯Ό μ¬μ©μΈ‘μ μ°κ²°μμΌ λκΈ°ννλ λ°©μμ΄λ€.<h6></p>
- MVC κΈ°λ°μ UIKit κ³Ό λ¬λ¦¬ SwiftUI λ MVVM ν¨ν΄μ κΈ°λ°μΌλ‘ νλ€. 
- SwiftUI λ Reactive Programming ν¨λ¬λ€μμ μ·¨νκ³  μλ€.
  - <p><h6>λ³νμ λ°λΌ λ°μ΄ν°λ₯Ό μ λ¬νκ³ , κ·Έμ λ°μν΄ μ μ ν μ΄λ²€νΈλ₯Ό μ€ννλ λ°μν νλ‘κ·Έλλ°</h6></p>

<br>

<p align="center">
  <img src="https://user-images.githubusercontent.com/101554627/167997945-40ba5e86-b4f2-4a15-ae18-ab11b2897cb6.png" alt="center" />
</p>

<br><br><br>

# M - Model
- Model μ ViewModel μ μν΄ μλλκ³  Model μ΄ μμμ λ§μΉλ©΄ ViewModel μκ² κ²°κ³Όλ₯Ό μλ €μ€λ€.
- Application μ λ°μ΄ν° λͺ¨λΈ, λ°μ΄ν° μ κ·Ό λ μ΄μ΄, λΉμ¦λμ€ λ‘μ§μ κ΄λ¦¬νλ€.


<br><br><br>

# V - View
- μ£Όλ‘ ViewController μ μμ±νλ€.
- μ¬μ©μ μ΄λ²€νΈλ₯Ό μμ νκ³ , λ°μ΄ν°λ₯Ό μκ°μ μΌλ‘ νννλ€.
- View μ Model μ μνΈμμ©μ΄ λΆκ°νκ³  ViewModel μ μν΄ λμλλ€.

<br><br><br>

# VM - ViewModel
- μ£Όμ λ‘μ§μ λ΄λΉνλ€.
- View μμ μμ ν μ΄λ²€νΈλ₯Ό μ²λ¦¬ν λ€ Model μ μλ°μ΄νΈ νκ³ , κ·Έ κ²°κ³Όλ₯Ό λ°μ View μ λ€μ μ λ¬ν΄μ UI λ₯Ό μλ°μ΄νΈ νλ€.
- κ°μ²΄λ₯Ό μ½κ² κ΄λ¦¬ν  μ μλ μ₯μ μ΄ μλ€.

<br><br><br>

# Data Binding
- Data Binding μ Model μ UI μμ κ°μ μ±ν¬λ₯Ό λ§μΆ°μ£Όλ κ²μ΄λ€.
- View μ λ‘μ§μ΄ λΆλ¦¬λμ΄ μμ΄λ ν μͺ½μ΄ λ°λλ©΄ λ€λ₯Έ μͺ½λ μλ°μ΄νΈκ° μ΄λ£¨μ΄μ Έ λ°μ΄ν°μ μΌκ΄μ±μ μ μ§ν  μ μλ€.
- iOS μμ λ°μ΄ν° λ°μΈλ©μ νλ λ°©λ²
  - <p><h6>KVO</h6></p>
  - <p><h6>Delegation</h6></p>
  - <p><h6>Functional Reactive Programming</h6></p>
  - <p><h6>Property Observer</h6></p>

<br><br><br>

# MVVM Pattern μ μμ
- κΈ°μ‘΄ μ½λ
```swift
class ViewController: UIViewController {
    //Outlets
    @IBOutlet weak var messageLabel: UILabel!
    @IBOutlet weak var userNameField: UITextField!
    @IBOutlet weak var passwordField: UITextField!
   
    var name: String
    var email: String
    var userName: String { return user.name }
    var email: String { return user.email }
    
    typealias authenticationLoginCallback = (_ status: Bool, _ message: String) -> Void //callback 
    
    var callback: authenticationLoginCallback?

    override func viewDidLoad() {
        super.viewDidLoad()
        self.messageLabel.isHidden = true
        // Do any additional setup after loading the view.
    }
    
    @objc func loginUser() {
        self.messageLabel.isHidden = true
        guard let userName = self.userNameField.text else { return }
        guard let password = self.passwordField.text else { return }
        authenticationUser(userName, password)//λ‘κ·ΈμΈ μ ν¨μ± κ²μ¬
        
      //callbackμ λ°λ₯Έ UIλ³ν 
       loginCompletion { [weak self] status, message in
            guard let self = self else { return }
            if status {
                self.messageLabel.text = "login success"
                self.messageLabel.isHidden = false
            } else {
                self.messageLabel.text = message
                self.messageLabel.isHidden = false
            }
        }
    }
    
        //λ‘κ·ΈμΈ μ ν¨μ± κ²μ¬ 
    func authenticationUser(_ email: String, _ password: String) {
        DispatchQueue.main.asyncAfter(deadline: DispatchTime.now() + 0.1) {
            if self.userName.count != 0 {
                if password.count != 0 {
                    self.verifyUser(self.userName, password)
                }else {
                    self.callback?(false, "password error")
                }
            }else {
                self.callback?(false, "user error")
            }
        }
    }
    //μ μ  νμΈ 
    fileprivate func verifyUser(_ email: String, _ password: String) {
        if userName == "test" && password == "1234" {
            user = User(name: userName, email: "\(userName)@gmail.com")
            self.callback?(true, "success")
        }else {
            self.callback?(false, "Please enter valid source")
        }
    }
    
  //λ‘κ·ΈμΈ μλ£μ callback λ©μλ 
    func loginCompletion(callBack: @escaping authenticationLoginCallback) {
        self.callback = callBack
    }
}
```
- MVVM Pattern μΌλ‘ λ³κ²½ν μ½λ
```swift
//Model

struct User {
  var name: String
  var email: String
}
```
```swift
// View

class ViewController: UIViewController {
    //Outlets
    @IBOutlet weak var messageLabel: UILabel!
    @IBOutlet weak var userNameField: UITextField!
    @IBOutlet weak var passwordField: UITextField!
   
  var viewModel = ViewModel()//ViewModel

    override func viewDidLoad() {
        super.viewDidLoad()
        self.messageLabel.isHidden = true
        // Do any additional setup after loading the view.
    }
    
    @objc func loginUser() {
        self.messageLabel.isHidden = true
        guard let userName = self.userNameField.text else { return }
        guard let password = self.passwordField.text else { return }
        viewModel.authenticationUser(userName, password)//λ‘κ·ΈμΈ μ ν¨μ± κ²μ¬
        
      //callbackμ λ°λ₯Έ UIλ³ν 
        viewModel.loginCompletion { [weak self] status, message in
            guard let self = self else { return }
            if status {
                self.messageLabel.text = "login success"
                self.messageLabel.isHidden = false
            } else {
                self.messageLabel.text = message
                self.messageLabel.isHidden = false
            }
        }
    }
}
```
```swift
//  ViewModel


class ViewModel: NSObject {
    var user: User! //Model 
    var userName: String { return user.name }
    var email: String { return user.email }
    
    typealias authenticationLoginCallback = (_ status: Bool, _ message: String) -> Void //callback 
    
    var callback: authenticationLoginCallback?
    
    //λ‘κ·ΈμΈ μ ν¨μ± κ²μ¬ 
    func authenticationUser(_ email: String, _ password: String) {
        DispatchQueue.main.asyncAfter(deadline: DispatchTime.now() + 0.1) {
            if self.userName.count != 0 {
                if password.count != 0 {
                    self.verifyUser(self.userName, password)
                }else {
                    self.callback?(false, "password error")
                }
            }else {
                self.callback?(false, "user error")
            }
        }
    }
    //μ μ  νμΈ 
    fileprivate func verifyUser(_ email: String, _ password: String) {
        if userName == "test" && password == "1234" {
            user = User(name: userName, email: "\(userName)@gmail.com")
            self.callback?(true, "success")
        }else {
            self.callback?(false, "Please enter valid source")
        }
    }
    
  //λ‘κ·ΈμΈ μλ£μ callback λ©μλ 
    func loginCompletion(callBack: @escaping authenticationLoginCallback) {
        self.callback = callBack
    }
    
}
```

<br><br><br>

# MVVM Pattern μ μ₯/λ¨μ 
### μ₯μ 
- View μ Model μ΄ μλ‘ μ ν μ°κ΄μ΄ μκΈ°μ λλ¦½μ±μ μ μ§ν  μ μλ€.
- λλ¦½μ±μ΄ μ μ§λμ΄ ν¨μ¨μ μΈ μ λνμ€νΈκ° κ°λ₯νλ€.
- ViewModel μμλ UIKit κ΄λ ¨ μ½λκ° μκ³  Controller μμ μμ‘΄μ±λ μκΈ° λλ¬Έμ μ λνμ€νΈ νκΈ°κ° μ’λ€.
- View μ ViewModel μ κ΄κ³λ N:1 κ΄κ³μ΄λ€.

### λ¨μ 
- μ΄λ³΄μμ κ²½μ° MVVM μ κ΅¬ννκΈ° μ΄λ ΅λ€.
- κ°λ¨ν UI μμ MVVM μ κ³Όνλ€.
- λ°μ΄ν° λ°μΈλ©μ΄ νμμ΄λ€.
- λ³΅μ‘ν΄μ§μλ‘ Controller μ²λΌ ViewModel μ΄ Massive ν΄μ§λ€.
- ν° Application μ κ²½μ° λ°μ΄ν° λ°μΈλ©μ΄ λ³΅μ‘νλ―λ‘ λλ²κΉμ΄ μ΄λ ΅λ€. 

<br><br><br>

# μ°Έμ‘°
- [λ₯³λ](https://velog.io/@ryuhyewon/MVVM-%EA%B0%9C%EB%85%90%EA%B3%BC-%EC%9E%A5%EB%8B%A8%EC%A0%90)
- [GomMinjaeλ](https://velog.io/@gomminjae/Swift-MVVM)
- [yoonbumtaeλ](http://yoonbumtae.com/?p=4215)
- [sh9404λ](https://lsh424.tistory.com/68)
