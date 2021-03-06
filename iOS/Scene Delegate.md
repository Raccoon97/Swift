# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [Scene Delegate](https://github.com/Raccoon97/Swift/blob/main/iOS/Scene%20Delegate.md#scene-delegate)
- [iOS12 κΉμ§μ App Delegate](https://github.com/Raccoon97/Swift/blob/main/iOS/Scene%20Delegate.md#ios12-%EA%B9%8C%EC%A7%80%EC%9D%98-app-delegate)
- [iOS13 μ΄νλ‘ λ°λ App Delegate](https://github.com/Raccoon97/Swift/blob/main/iOS/Scene%20Delegate.md#ios13-%EC%9D%B4%ED%9B%84%EB%A1%9C-%EB%B0%94%EB%80%90-app-delegate)
- [Scene μ΄λ?](https://github.com/Raccoon97/Swift/blob/main/iOS/Scene%20Delegate.md#scene-%EC%9D%B4%EB%9E%80)
- [Scene Delegate μ λ©μλ νΈμΆ](https://github.com/Raccoon97/Swift/blob/main/iOS/Scene%20Delegate.md#scene-delegate-%EC%9D%98-%EB%A9%94%EC%86%8C%EB%93%9C-%ED%98%B8%EC%B6%9C)
- [μ¬ν - iOS μμμ Scene](https://github.com/Raccoon97/Swift/blob/main/iOS/Scene%20Delegate.md#%EC%8B%AC%ED%99%94---ios-%EC%97%90%EC%84%9C%EC%9D%98-scene)
  - [SceneDelegate μ μΆν λ°°κ²½](https://github.com/Raccoon97/Swift/blob/main/iOS/Scene%20Delegate.md#scenedelegate-%EC%9D%98-%EC%B6%9C%ED%98%84-%EB%B0%B0%EA%B2%BD)
  - [λͺμ  νμΈ](https://github.com/Raccoon97/Swift/blob/main/iOS/Scene%20Delegate.md#%EB%AA%85%EC%A0%9C-%ED%99%95%EC%9D%B8)
  - [iPad](https://github.com/Raccoon97/Swift/blob/main/iOS/Scene%20Delegate.md#ipad)
  - [iPhone](https://github.com/Raccoon97/Swift/blob/main/iOS/Scene%20Delegate.md#iphone)
  - [κ²°κ³Ό](https://github.com/Raccoon97/Swift/blob/main/iOS/Scene%20Delegate.md#%EA%B2%B0%EA%B3%BC)

<br><br><br>

# Scene Delegate
- νλ©΄μ λ¬΄μ( Window/ Scene )μ λ³΄μ¬μ€μ§ κ΄λ¦¬νλ μ­ν μ νλ€.

<br>

## iOS12 κΉμ§μ App Delegate
- νλμ App μ νλμ Window μ΄λ€.

<br>

![image](https://user-images.githubusercontent.com/101554627/175017828-1a18ddab-1c1c-4804-9baf-72127715745c.png)

## iOS13 μ΄νλ‘ λ°λ App Delegate
- Window μ κ°λμ΄ Scene μΌλ‘ λμ²΄λκ³  νλμ App μμ μ¬λ¬ κ°μ Scene μ κ°μ§ μ μκ² λμλ€.

<br>

![image](https://user-images.githubusercontent.com/101554627/175017838-36ca3dfc-e158-4248-a4d6-9dcc902e2181.png)
- μλ μμμ κ°μ΄ νλμ λ©λͺ¨μ₯ App μμ 2κ°μ Scene μ λμμ λμΈ μ μλ€.

<br>

![image](https://user-images.githubusercontent.com/101554627/175018913-8ba00d8a-0d21-41aa-bf81-b6bec1437e1f.png)

- AppDelegate μ μ­ν  μ€ UI μ μνλ₯Ό μ μ μλ UILifeCycle μ λν λΆλΆμ SceneDelegate κ° νκ² λμλ€.

<br>

![image](https://user-images.githubusercontent.com/101554627/175018354-c886ccf0-f66c-438a-be3f-81b08f3e8472.png)
- AppDelegate μ Session LifeCycle μ λν μ­ν μ΄ μΆκ°λμλ€.
- Scene Session μ΄ μμ±λκ±°λ μ­μ λ  λ AppDelegate μ μλ¦¬λ λ λ©μλκ° μΆκ°λμμΌλ©° App μμ μμ±ν λͺ¨λ  Scene μ μ λ³΄λ₯Ό κ΄λ¦¬νλ€.
<br>

![image](https://user-images.githubusercontent.com/101554627/175018791-74f86477-1706-4dd0-a055-17ff4bfed4dd.png)


## Scene μ΄λ?
- UIKit λ UIWindowScene κ°μ²΄λ₯Ό μ¬μ©νλ App UI μ κ° μΈμ€ν΄μ€λ₯Ό κ΄λ¦¬νλ€.
- Scene μλ UI μ νλμ μΈμ€ν΄μ€λ₯Ό λνλ΄λ Windows μ ViewControllers κ° λ€μ΄μλ€.
- κ° Scene μ ν΄λΉνλ UIWindowSceneDelegate κ°μ²΄λ₯Ό κ°μ§κ³  μμΌλ©° μ΄ κ°μ²΄λ UIKit κ³Ό App κ°μ μνΈ μμ©μ μ‘°μ νλ λ° μ¬μ©λλ€.
- Scene λ€μ κ°μ λ©λͺ¨λ¦¬μ App νλ‘μΈμ€ κ³΅κ°μ κ³΅μ νλ©΄μ μλ‘ λμμ μ€νλλ€.
- νλμ App μ μ¬λ¬ Scene κ³Ό SceneDelegate κ°μ²΄λ₯Ό λμμ νμ±νν  μ μλ€.

<br>

## Scene Delegate μ λ©μλ νΈμΆ

<br>

### scene(_ : willConnectTo: options: )
```swift
func scene(_ scene: UIScene, 
           willConnectTo session: UISceneSession, 
           options connectionOptions: UIScene.ConnectionOptions) {
  guard let _ = (scene as? UIWindowScene) else { return }
}
// μ μΌ μ²μμΌλ‘ νΈμΆλλ λ©μλλ‘ μ²« Content View, μλ‘μ΄ UIWindow λ₯Ό μμ±νκ³  Window μ RootViewController λ₯Ό μ€μ νλ€.
// μ΄ λμ Window λ μ¬μ©μκ° λ³΄λ Window κ° μλ App μ΄ λμνλ ViewPort μ΄λ€.
// μ²« View λ₯Ό λ§λ€ λ μ°μ΄μ§λ§ κ³Όκ±°μ Disconnected λ UI λ₯Ό λλλ¦΄ λ μ¬μ©νκΈ°λ νλ€.
```

<br>

### sceneWillEnterForeground(_ :)
```swift
func sceneWillEnterForeground(_ scene: UIScene) {
}
// μ²« View κ° μμ±λλ©΄ sceneWillEnterForeground κ° νΈμΆλλ€.
// Background -> Foreground μΈ κ²½μ°μ μ΅μ΄ Active μνκ° λμμ λ νΈμΆλλ€.
```

<br>

### sceneDidBecomeActive(_ :)
```swift
func sceneDidBecomeActive(_ scene: UIScene) {
}
// Scene μ΄ μ€μ λκ³  νλ©΄μ λ³΄μ¬μ§λ©΄μ μ¬μ© μ€λΉκ° λλ μνμ΄λ€.
// Inactive -> Active μνμμ νΈμΆλλ€.
```

<br>

### sceneWillResignActive(_ :)
```swift
func sceneWillResignActive(_ scene: UIScene) {
}
// Active ν μνμμ Inactive μνλ‘ λΉ μ§ λ νΈμΆλλ€.
// App μ¬μ© μ€ μ νκ° μ€λ κ² μ²λΌ μμ Interruption λλ¬Έμ νΈμΆλ  μ μλ€.
```

<br>

### sceneDidEnterBackground(_ :)
```swift
func sceneDidEnterBackground(_ scene: UIScene) {
}
// Scene μ΄ Foreground μμ Background λ‘ μ νλ  λ νΈμΆλλ€.
// λ€μ Foreground λ‘ λμμ¬ λ λ³΅μλ  μ μκ² μν μ λ³΄λ₯Ό μ μ₯νκ±°λ, λ°μ΄ν°λ₯Ό μ μ₯, κ³΅μ  μμμ λ°ννλ μΌμ νλ€.
```

<br>

### sceneDidDisconnect(_ :)
```swift
func sceneDidDisconnect(_ scene: UIScene) {
}
// Scene μ΄ Background κ° λμμ λ μμ€νμ΄ μμμ νλ³΄νκΈ° μν΄ Disconnect ν  μ μλ€ --> Suspended
// Scene μ΄ ν΄λΉ λ©μλλ‘ μ λ¬λλ©΄ Session μ΄ λμ΄μ§κ²λλ©°, Disconnect λ App μ μ’λ£μλ λ€λ₯΄λ€
```

<br>

<br>

# μ¬ν - iOS μμμ Scene
- SceneDelegate λ μ μκ²Όλμ§ μμλ³΄μ.
- κ³Όμ° iPhone μ μ¬μ©ν  λμλ μμ λͺμ κ° μ°ΈμΈμ§ νμΈν΄λ³΄λλ‘ νμ.
- νλμ νλ‘μ νΈλ₯Ό μ¬μ©ν΄μ iPad Pro 3rd, iPhone 12 Pro λ κ°μ§ κΈ°κΈ°μ λν΄μ νμ€νΈλ₯Ό μ§νν΄λ³΄μλ€.

<br>

## SceneDelegate μ μΆν λ°°κ²½
- iOS 12 κΉμ§λ AppDelegate κ° App μ μ΄λ²€νΈλ₯Ό μλ¦¬κ±°λ UI μνλ₯Ό μλ¦¬λ μ­ν μ νλ€.
  - App λ€μ΄ νλμ νλ‘μΈμ€μ νλμ UI μΈμ€ν΄μ€λ₯Ό κ°κ³  μκΈ° λλ¬Έμ AppDelegate νλλ‘ μΆ©λΆνλ€.
- iOS 13 λΆν°λ νλμ νλ‘μΈμ€κ° μ¬λ¬ UI μΈμ€ν΄μ€λ₯Ό κ°μ§ μ μλ€.
  - νλ‘μΈμ€ μ΄λ²€νΈμ Lift Cycle μ κ²½μ° κ·Έλλ‘ AppDelegate κ° λ΄λΉνλ€.
- _1:1 μΈ AppDelegate λ§κ³  1:N μ΄ λλ, UI LifeCycle κ΄λ¦¬κ° νμνκΈ° λλ¬Έμ SceneDelegate κ° μΆννκ² λμλ€._

<br>
<br>

## λͺμ  νμΈ
- Info.plist μ Enable Multiple Windows λ₯Ό YES λ‘ λ³κ²½μν¨λ€.
- AppDelegate μμ multipleScene μ¬λΆμ κΈ°κΈ° μ λ³΄λ₯Ό νμΈνλ€.
- SceneDelegate μμ Scene μ μμ±ν  λ λ§λ€ μΆλ ₯λκ² νλ€.

<br>

## iPad
- νμΈ κ²°κ³Ό 
  - supportsMultipleScene = true
  - Enable Multiple Windows = YES
  - Scene μ μλ‘ λ§λ€ λ λ§λ€ SceneDelegate μμ μΆλ ₯μ΄ λλ€.

![αα³αα³αα΅α«αα£αΊ 2022-07-01 αα©αα? 8 02 42](https://user-images.githubusercontent.com/101554627/176884985-d323acf4-d20c-43e8-aa18-e20efd92a6cc.png)


<br><br>

## iPhone
- νμΈ κ²°κ³Ό 
  - supportsMultipleScene = false
  - Enable Multiple Windows = YES
  - Scene μ νλ μ΄μ λ§λ€ μ μλ€.

![αα³αα³αα΅α«αα£αΊ 2022-07-01 αα©αα? 8 05 09](https://user-images.githubusercontent.com/101554627/176884995-35fb4f49-02b8-4cbd-ae80-8098f45a8389.png)

<br><br>

## κ²°κ³Ό
- νλ‘μ νΈ μ€μ  μμμ Enable Multiple Windows λ νμ±νκ° κ°λ₯νλ©° iPhone, iPad λ λ€ μ μ©λλ€.
- νμ§λ§ μ€μ  App κ΅¬λ μ AppDelegate μμ supportsMultipleScene μ iPhone = false, iPad = true λ‘ κ°λ¦¬κ² λλ€.
- iOS 13 μ΄νλ‘ νλμ μ±μ΄ μ¬λ¬ κ°μ Scene μ κ°μ μ μλ€κ³  νμ§λ§, μ€μ λ‘ iPadOS λ§ κ°λ₯νλ€.
- νμ¬ μΆμλ iPhone μ© Split View App λ€μ Web Browser κΈ°λ°μΌλ‘ νλμ νμ΄μ§λ₯Ό λλμ΄ κ°κ° App μ μ¬μ©ν  μ μκ² ν΄μ€λ€.
  - μ€μ  κΈ°κΈ°μμ κ΅¬λλλ App μ΄ μλλ©°, Web μΌλ‘ μ κ·Όμ΄ κ°λ₯ν App λ€λ§ κ°λ₯νλ€.


<br>

<br>

<br>

# μ°Έμ‘°
- [Jakeλ](https://ios-development.tistory.com/53)
- [Sueatyλ](https://sueaty.tistory.com/134)
- [Lenaλ](https://velog.io/@dev-lena/iOS-AppDelegate%EC%99%80-SceneDelegate)
- [iPadOS Tutorial](https://www.raywenderlich.com/5814609-adopting-scenes-in-ipados)
