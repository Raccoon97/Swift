# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [UINavigationController](https://github.com/Raccoon97/Swift/blob/main/iOS/UINavigationController.md#uinavigationcontroller)
  - [UINavigationViewController μμ κ΄λ¦¬νλ κ°μ²΄](https://github.com/Raccoon97/Swift/blob/main/iOS/UINavigationController.md#uinavigationviewcontroller-%EC%97%90%EC%84%9C-%EA%B4%80%EB%A6%AC%ED%95%98%EB%8A%94-%EA%B0%9C%EC%B2%B4)
- [UINavigationController μ μ¬μ©](https://github.com/Raccoon97/Swift/blob/main/iOS/UINavigationController.md#uinavigationcontroller-%EC%9D%98-%EC%82%AC%EC%9A%A9)
  - [StoryBoard κ΅¬ν](https://github.com/Raccoon97/Swift/blob/main/iOS/UINavigationController.md#storyboard-%EA%B5%AC%ED%98%84)
  - [Code κ΅¬ν](https://github.com/Raccoon97/Swift/blob/main/iOS/UINavigationController.md#code-%EA%B5%AC%ED%98%84)


<br><br><br>

# UINavigationController
```swift
@MainActor class UINavigationController : UIViewController
```

- Navigation μΈν°νμ΄μ€μμ 1κ° μ΄μμ νμ View Controller λ₯Ό κ΄λ¦¬νλ Container View Controller μ΄λ€.
- Stack κΈ°λ°μ΄λ©°, ν λ²μ νλμ View Controller λ§ λ³΄μ¬μ§κ³  Push/ Pop μ ν΅ν΄ λ³΄μ¬μ§ View Controller λ₯Ό κ²°μ νλ€.
- μ²« λ²μ§Έ View Controller λ Root View Controller μ΄λ©° Stack μ λ§¨ μλ ν­λͺ©μ λνλΈλ€.
- λ§μ§λ§ View Controller λ Stack μ λ§¨ μ ν­λͺ©μ΄λ©°, νμ¬ νμλ View Controller μ΄λ€.

<br>

<p align="center">
<img width="960" alt="img1" src="https://user-images.githubusercontent.com/101554627/176487930-094feaca-9a90-45d7-a556-b8659c49073e.png">
</p>
  
<p align="center">
<img width="960" alt="img2" src="https://user-images.githubusercontent.com/101554627/176492414-bd3bc7ca-fc33-473a-a7bf-6a92cc8f4aa8.png">
</p>
  
<br><br>

## UINavigationViewController μμ κ΄λ¦¬νλ κ°μ²΄

![image](https://user-images.githubusercontent.com/101554627/176494081-c5fdcaaf-fe17-4e39-a964-cf394613209b.png)

<br>

- ViewControllers
  - UINavigationController λ μ¬λ¬ κ°μ View Controller λ₯Ό κ΄λ¦¬ν  μ μλ Contrainer View Controller μ΄λ€.
  - Navigation Stack μ μμΈ View Controller λ€μ λ°°μ΄ ννλ‘ κ°μΌλ©°, ν΄λΉ λ°°μ΄μ push, pop ννλ‘ κ΄λ¦¬λλ€.

<br>

- navigationBar < UINavigationBar >
  - μ±μ μ¬μ©ν¨μ μμ΄ μλ¨μ νμ΄ν, λ€λ‘κ°κΈ°, μ€μ  λ± UI μμλ€μ μμ­μ Navigation Bar λΌκ³  νλ€.
  - UINavigationController λ₯Ό μ¬μ©νλ©΄ λ°λ‘ UI λ₯Ό μΆκ°ν  νμ μμ΄ μ¬μ©ν  μ μλ€.

<br>

- toolbar < UIToolbar >
  - μ£Όλ‘ μ± νλ¨μ μμΉν μ¬λ¬ λκ΅¬μ λͺ¨μμ΄λ€.
  - κΈ°λ³Έμ μΌλ‘ UINavigationController μμλ μ¨κΉμ²λ¦¬( isToolbarHidden = True ) λμ΄μμ§λ§, μ¨κΉμ ν΄μ νκ³  ν΄λΉ μμ­ μ€μ μ΄ κ°λ₯νλ€.

<br>

- delegate < Custom Delegate Object >
  - UITableViewDelegate μ²λΌ UINavigationController μλ νΉμ  Event μμ μ¬μ©ν  μ μλ delegate κ° μ μΈλμ΄ μλ€.
  - νΉμ  ViewController λ₯Ό λ³΄μ¬μ£Όκ³  μ¬λΌμ§κ² νκ±°λ, μ»€μ€ν μ λλ©μ΄μμ μ κ³΅νλ€. 
  - UINavigationControllerDelegate νλ‘ν μ½μ μ€μν΄μΌ νλ€.

<br><br>

# UINavigationController μ μ¬μ©

<br>

## StoryBoard κ΅¬ν
- StoryBoard μ Root ViewController μ Child ViewController κ° μλ€κ³  κ°μ νλ€.
- Root ViewController μ Go Child λ²νΌμ ν­νλ©΄ Child ViewController κ° λ³΄μ΄κ² λλ€.
  - μ΄ λ, Go Child λ²νΌμ Segue λ Push λ‘ ν΄μ€λ€.

<br>

<p align="center">
<img width="600" alt="αα³αα³αα΅α«αα£αΊ 2022-06-30 αα©αα? 6 41 14" src="https://user-images.githubusercontent.com/101554627/176646159-d9f44469-0ada-49d3-bd40-7cef0814252f.png">
</p>

<br>

- Root ViewController λ₯Ό μ νν λ€ Editor -> Embed In -> Navigation Controller λ₯Ό μ ννλ€.

<br>

<p align="center">
<img width="600" alt="αα³αα³αα΅α«αα£αΊ 2022-06-30 αα©αα? 6 43 35" src="https://user-images.githubusercontent.com/101554627/176646347-2eed793c-cfab-4ca1-997e-2fba5f104cbb.png">
</p>

<br>

- μ μμ μΌλ‘ Navigation Controller κ° μΆκ°λμκ³  Child ViewController μμλ < back νμλ₯Ό νμΈν  μ μλ€.

<br>

<p align="center">
<img width="946" alt="αα³αα³αα΅α«αα£αΊ 2022-06-30 αα©αα? 6 47 40" src="https://user-images.githubusercontent.com/101554627/176647578-5df3ede1-348b-48ed-9b8f-e9124a2454c0.png">
</p>

<br>

- Navigation Controller λ₯Ό μ μ©ν΄μ Root ViewController μ Child ViewController λ₯Ό νμνλ κ²°κ³Ό

<p align="center">
<img width="300" alt="ezgif-2-0dad8dc71a" src="https://user-images.githubusercontent.com/101554627/176648998-6e19f16a-b0de-4127-8ce6-37a85892149e.gif">
</p>


<br><br>

## Code κ΅¬ν

```swift
import UIKit


// λ²νΌμ 3κ°μ§ μμΉλ₯Ό λ―Έλ¦¬ μ§μ .
let statBtnRect = CGRect(x: 50, y: 100, width: 300, height: 52)
let commonBtnRect = CGRect(x: 100, y: 100, width: 200, height: 52)
let dimissBtnRect = CGRect(x: 100, y: 162, width: 200, height: 52)

// λ²νΌμ λ§λ€κ³  View μ λμ°λ ν¨μ
// 3 κ°μ λ·°μ»¨νΈλ‘€λ¬μ κ²ΉμΉλ λΆλΆμ΄ λ§μ μ½λκ° κΈΈμ΄μ Έμ μλ¨μΌλ‘ λΉΌλμλ€.
func makeButton(
                _ viewSelf: UIViewController ,  // viewSelf - κ° ViewController μΈμ€ν΄μ€λ₯Ό μ¬μ©νκΈ° μν¨
                _ view_: UIView,                // view     - κ° ViewController μ View λ₯Ό μ¬μ©νκΈ° μν¨
                _ btn: UIButton,                // btn      - λ²νΌμ μμΉμ λͺ¨μμ μ§μ ν΄μ View μ λμ°κΈ° μν¨
                _ title: String,                // title    - λ²νΌμ Title μ λ€μνκ² μ¬μ©νκΈ° μν¨
                _ function: Selector,           // function - μ½λλ‘ κ΅¬νν¨μ λ°λΌ objc ν¨μλ₯Ό μμ±νκ³  μ¬μ©νκΈ° μν¨
                _ rect: CGRect                  // rect     - λ²νΌμ μμΉλ₯Ό λ€μνκ² μ§μ νκΈ° μν¨
                ) {
    
    // λ²νΌμ Title μ μ§μ νλ€.
    btn.setTitle(title, for: .normal)
    
    // λ²νΌμ View μ μΆκ°νλ€.
    view_.addSubview(btn)
    
    // λ²νΌμ λ°°κ²½μμ μ§μ νλ€.
    btn.backgroundColor = .clear
    
    // λ²νΌμ Title μκΉμ μ§μ νλ€.
    btn.setTitleColor(.systemBlue, for: .normal)
    
    // λ²νΌμ μμΉλ₯Ό μ§μ νλ€.
    btn.frame = rect
    
    // λ²νΌμ΄ νΈμΆλλ κ³³κ³Ό μ΄λ€ μμμ, μ΄λ€ μ΄λ²€νΈκ° λ°μλμμ λ νκ² λλμ§ μ§μ νλ€.
    btn.addTarget(viewSelf, action: function, for: .touchUpInside)
}


// @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@

// View μμμ§μ , λ²νΌμ λλ¬ λ€λΉκ²μ΄μ μ»¨νΈλ‘€λ¬λ₯Ό μ¬μ©νλ€.
class ViewController: UIViewController {
    
    // ν­νλ©΄ λ€λΉκ²μ΄μ μ»¨νΈλ‘€λ¬λ₯Ό μ¬μ©νκ²λλ λ²νΌ
    private let button = UIButton()
    
    override func viewDidLoad() {
        super.viewDidLoad()

        // λ²νΌμ λ§λ€μ΄ View μ λμμ€λ€.
        makeButton(self, view, button, "λ€λΉκ²μ΄μ μ»¨νΈλ‘€λ¬ μ¬μ©νκΈ°", #selector(didTapButton_ToNav), statBtnRect)
    }
        
    // λ²νΌμ λλ μ λ μ€νλλ ν¨μ
    @objc private func didTapButton_ToNav() {
        
        // Root λ·°μ»¨νΈλ‘€λ¬λ RootViewController μ΄λ€.
        let rootVC = RootViewController()
        
        // μ§μ ν rootVC λ₯Ό κ°κ³  UINavigationController λ₯Ό μ μΈν΄μ€λ€.
        let navVC = UINavigationController(rootViewController: rootVC)
        
        // FullScreen μ€νμΌλ‘ Modal νκ² λ€κ³  λ―Έλ¦¬ μ€μ ν΄μ€λ€.
        navVC.modalPresentationStyle = .fullScreen
        
        // UINavigationController λ₯Ό κ°λ Root λ·°μ»¨νΈλ‘€λ¬λ₯Ό λ³΄μ¬μ€λ€.
        present(navVC, animated: true)
    }
    

}


// @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@

// Root λ·°μ»¨νΈλ‘€λ¬, λ€λΉκ²μ΄μ μ»¨νΈλ‘€λ¬μ μ΅μμ λ·°
class RootViewController: UIViewController {
    
    // λ€μ λ·°μ»¨νΈλ‘€λ¬λ₯Ό Push ν  λ²νΌκ³Ό λ€λΉκ²μ΄μ μ»¨νΈλ‘€λ¬λ₯Ό λλ΄λ λ²νΌ
    private let button_PushView = UIButton()
    private let button_Dimiss = UIButton()
    
    override func viewDidLoad() {
        super.viewDidLoad()

        // λ°°κ²½μ΄ μμ κ²½μ° View κ° μ¬λΌμ€μ§ μμ, Title μ μκ΄ μμ
        view.backgroundColor = .white
        title = "λ€λΉκ²μ΄μ μ»¨νΈλ‘€λ¬"
        
        // λ²νΌ 2κ°λ₯Ό λ§λ€μ΄ View μ λμμ€λ€. Push, Dismiss
        makeButton(self, view, button_PushView, "λ€λ₯Έ λ·°μ»¨νΈλ‘€λ¬ Push νκΈ°", #selector(didTapButton_PushView), commonBtnRect)
        makeButton(self, view, button_Dimiss, "λμκ°κΈ°", #selector(didTapButton_Dismiss), dimissBtnRect)
    }
    
    // λ€λ₯Έ λ·°μ»¨νΈλ‘€λ¬λ₯Ό Push νλ ν¨μ
    @objc private func didTapButton_PushView() {
        let vc = SecondViewController()
        navigationController?.pushViewController(vc, animated: true)
    }
    
    // λ€λΉκ²μ΄μ μ»¨νΈλ‘€λ¬ μμ μ μΌλ‘ λμκ°λ ν¨μ
    @objc private func didTapButton_Dismiss(){
        dismiss(animated: true)
    }
    
}


// @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@

// λ λ²μ§Έ λ·°μ»¨νΈλ‘€λ¬
class SecondViewController: UIViewController {
    
    // νμ¬ λ·°μ»¨νΈλ‘€λ¬λ₯Ό Pop ν  λ²νΌ
    private let button = UIButton()
    
    override func viewDidLoad() {
        super.viewDidLoad()
        
        // λ°°κ²½μ΄ μμ κ²½μ° View κ° μ¬λΌμ€μ§ μμ, Title μ μκ΄ μμ
        view.backgroundColor = .white
        title = "2λ²μ§Έ μ₯"
        
        // λ²νΌμ λ§λ€μ΄ View μ λμμ€λ€. Pop
        makeButton(self, view, button, "νμ¬ λ·°μ»¨νΈλ‘€λ¬ PopνκΈ°", #selector(didTapButton_PopView), commonBtnRect)
    }
    
    // νμ¬ λ·°μ»¨νΈλ‘€λ¬λ₯Ό Pop νλ ν¨μ
    @objc private func didTapButton_PopView() {
        navigationController?.popViewController(animated: true)
    }
}


```

- μ μ½λλ₯Ό μ€ννκ² λλ©΄ μλμ κ°μ κ²°κ³Όλ₯Ό μ»μ μ μλ€.
- λΆνμν μ½λλ₯Ό μ μΈνκΈ° μν΄ νμν λ²νΌκ³Ό λΌλ²¨λ§ λ£μ΄μ μ΄λΌνλ€..

<p align="center">
<img width="300" alt="μ½λκ΅¬νgif" src="https://user-images.githubusercontent.com/101554627/176740506-da22913e-5311-45a0-896d-c4f675846e95.gif">
</p>


<br><br><br>


# μ°Έμ‘°
- [Apple Developer Documentation](https://developer.apple.com/documentation/uikit/uinavigationcontroller)
- [iseeu95λ](https://velog.io/@iseeu95/UINavigationController-%EC%97%90-%EB%8C%80%ED%95%B4)
- [ν΅μ€λ](https://tong94.tistory.com/26)
