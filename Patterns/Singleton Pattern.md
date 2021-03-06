# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [Singleton Pattern](https://github.com/Raccoon97/Swift/blob/main/Patterns/Singleton%20Pattern.md#singleton-pattern)
- [Singleton Pattern μ μμ](https://github.com/Raccoon97/Swift/blob/main/Patterns/Singleton%20Pattern.md#singleton-pattern-%EC%9D%98-%EC%98%88%EC%8B%9C)
  - [iOS μμ μ¬μ©μ€μΈ Singleton](https://github.com/Raccoon97/Swift/blob/main/Patterns/Singleton%20Pattern.md#ios-%EC%97%90%EC%84%9C-%EC%82%AC%EC%9A%A9%EC%A4%91%EC%9D%B8-singleton)
  - [Singlton Class μμ± λ°©λ²](https://github.com/Raccoon97/Swift/blob/main/Patterns/Singleton%20Pattern.md#singlton-class-%EC%83%9D%EC%84%B1-%EB%B0%A9%EB%B2%95)
  - [Singleton μ¬μ© μ](https://github.com/Raccoon97/Swift/blob/main/Patterns/Singleton%20Pattern.md#singleton-%EC%82%AC%EC%9A%A9-%EC%98%88)
- [Singleton Pattern μ μ₯/λ¨μ ](https://github.com/Raccoon97/Swift/blob/main/Patterns/Singleton%20Pattern.md#singleton-pattern-%EC%9D%98-%EC%9E%A5%EB%8B%A8%EC%A0%90)

<br><br><br>

# Singleton Pattern
- ν κ°μ ν΄λμ€λ‘ λ§λλ μΈμ€ν΄μ€λ λ¨ νκ°μ¬μΌλ§ νλ€λ κ·μΉμ κ°λλ€.
- νΉμ  μ©λλ‘ κ°μ²΄λ₯Ό νλλ§ μμ±νμ¬, κ³΅μ©μΌλ‘ μ¬μ©νκΈ° μν λμμΈ ν¨ν΄μ΄λ€.
- μ νλ¦¬μΌμ΄μ λ΄ νΉμ  ν΄λμ€μ μΈμ€ν΄μ€κ° νλλ§ μ‘΄μ¬νκΈ° λλ¬Έμ κ°μ²΄κ° λΆνμνκ² μ¬λ¬ κ° λ§λ€μ΄μ§ νμκ° μλ κ²½μ°μ μ¬μ©νλ€.
- νκ²½μ€μ , λ€νΈμν¬ μ°κ²°μ²λ¦¬, λ°μ΄ν° κ΄λ¦¬ λ±μ μ¬μ©λλ€.
- λ©ν° μ€λ λ νκ²½μμλ λμμ μ±κΈν€ κ°μ²΄λ₯Ό μ°Έμ‘°ν  κ²½μ° μμΉ μλ κ²°κ³Όλ₯Ό κ°μ Έμ¬ μ μκΈ°μ μνμ±μ κ³ λ €ν΄μΌ νλ€.
- κΈ°μ‘΄ μΈμ€ν΄μ€λ³λ‘ μ°Έμ‘°νλ λ·°μ»¨νΈλ‘€λ¬λ€

<img width="960" alt="αα³αα¦αα¦α«αα¦αα΅αα§α«1" src="https://user-images.githubusercontent.com/101554627/169533707-515da57a-1d9d-4bad-9f1b-92f28bb4fd10.png">

- Singleton μ μ¬μ©νμ¬ νλμ μΈμ€ν΄μ€λ₯Ό μ°Έμ‘°νλ λ·°μ»¨νΈλ‘€λ¬λ€

<img width="960" alt="αα³αα¦αα¦α«αα¦αα΅αα§α«12" src="https://user-images.githubusercontent.com/101554627/169533713-570845ed-5b63-4f31-b7bb-ddc8593b7bb0.png">


<br><br><br>

# Singleton Pattern μ μμ

### iOS μμ μ¬μ©μ€μΈ Singleton
```swift
// νλμ¨μ΄ κΈ°λ° λμ€νλ μ΄μ κ΄λ ¨λ μμ±μ κ΄λ¦¬νλ ν΄λμ€
let screen = UIScreen.main

// Key-Value ννλ‘ κ°λ¨ν λ°μ΄ν°λ₯Ό μ μ₯νκ³  κ΄λ¦¬ν  μ μλ μΈν°νμ΄μ€λ₯Ό μ κ³΅νλ λ°μ΄ν°λ² μ΄μ€ ν΄λμ€
let userDefault = UserDefaults.standard

// iOS μμ μ€νλλ μ€μμ μ΄ μ΄νλ¦¬μΌμ΄μ κ°μ²΄
let application = UIApplication.shared

// μ νλ¦¬μΌμ΄μ νμΌ μμ€νμ κ΄λ¦¬νλ ν΄λμ€
let fileManager = FileManager.default

// λ±λ‘λ μλμ μ λ³΄λ₯Ό μ¬μ©ν  μ μκ² ν΄μ£Όλ ν΄λμ€
let notification = NotificationCenter.default

// URL μΈμμ κ΄λ¦¬νλ ν΄λμ€
let urlSession = URLSession.shared
```

### Singlton Class μμ± λ°©λ²
- static let μΌλ‘ μΈμ€ν΄μ€λ₯Ό ν λΉν΄μ£Όλ©΄ λμ΄λ€.
- μΈμ€ν΄μ€κ° μΆκ°λ‘ μμ±λλ κ²μ λ°©μ§νκΈ° μν΄ init() μ μ κ·Ό μ μ΄μλ₯Ό private λ‘ μ μΈνλ€.
```swift
class SingletonClass {
  static let shared = SingletonClass()
  private init() {}
}
```
### Singleton μ¬μ© μ
- Application μ μ λ³΄λ₯Ό μ μ₯νκ³  μλ AppInfo ν΄λμ€λ₯Ό Singleton μΌλ‘ μμ±ν μ½λ
```swift
class AppInfo {
  static let shared = AppInfo()
	private init() {}
 
	var mainInfo: [String : Any]? {
		guard let info = Bundle.main.infoDictionary else {
			return nil
		}
		return info
	}
 
	var name: String? {
		self.mainInfo?["CFBundleName"] as? String
	}
 
	var scheme: String? {
		guard let urlTypes = self.mainInfo?["CFBundleURLTypes"] as? [AnyObject],
			let urlTypeDictionary = urlTypes.first as? [String: AnyObject],
			let urlSchemes = urlTypeDictionary["CFBundleURLSchemes"] as? [AnyObject],
			let scheme = urlSchemes.first as? String else { return nil }
		return scheme
	}
 
	var version: String? {
		self.mainInfo?["CFBundleShortVersionString"] as? String
	}
}

let appInfo = AppInfo.shared
// appInfo λ³μμ AppInfo ν΄λμ€μ shared μΈμ€ν΄μ€λ₯Ό κ°μ Έμ¨λ€.

if let appName = appInfo.name,
	let appScheme = appInfo.scheme,
	let appVersion = appInfo.version {
		print("appName: \(appName)")
		print("appScheme: \(appScheme)")
		print("appVersion: \(appVersion)")
}
```

<br><br><br>

# Singleton Pattern μ μ₯/λ¨μ 
### μ₯μ 
- μΈμ€ν΄μ€λ₯Ό μ΅μ΄ 1νλ§ μμ±νλ―λ‘ λ©λͺ¨λ¦¬μ μ±λ₯ μΈ‘λ©΄μμ ν¨μ¨μ΄ μ’λ€.
- ν΄λμ€ κ° λ°μ΄ν° κ³΅μ κ° μ½λ€.
- μΈμ€ν΄μ€κ° 1κ°λΌλ κ²μ λ³΄μ¦λ°λλ€. (Thread Safe)
>- Thread Safe --> μ¬λ¬ μ€λ λμμ μ΄λ€ κ°μ²΄μ λν΄ λμμ μ κ·Όμ΄ μ΄λ£¨μ΄μ Έλ νλ‘κ·Έλ¨μ λμμ μ΄μμ΄ μλ κ² 

### λ¨μ 
- Singleton μΈμ€ν΄μ€κ° λλ¬΄ λ§μ μΌμ νκ±°λ λ§μ λ°μ΄ν°λ₯Ό κ³΅μ μν¬ κ²½μ° λ€λ₯Έ ν΄λμ€μ μΈμ€ν΄μ€λ€ κ°μ κ²°ν©λκ° λμμ Έ κ°λ°©-νμ μμΉμ μλ°°νκ² λλ€.
>- μμ κ³Ό νμ€νΈκ° μ΄λ €μμ§λ κ²°κ³Όλ₯Ό λ³λλ€.
- λ©ν°μ€λ λ νκ²½μμ μΈμ€ν΄μ€κ° 2κ° μμ±λ  κ°λ₯μ±μ΄ μ‘΄μ¬νλ©° κ·Έ λμλ Thread Safe νμ§ μλλ€λ μνμ±μ΄ μλ€.
>- Singleton λ΄λΆμ κ°μ²΄μ λ°μ΄ν°λ₯Ό λκΈ°μ μΌλ‘ μ²λ¦¬νμ§ μμΌλ©΄ κΌ¬μ¬λ²λ¦΄ κ°λ₯μ±λ μ‘΄μ¬νλ€.
- μ¬κΈ°μ κΈ°μ μ½κ² μ κ·Όν  μ μκΈ° λλ¬Έμ μμ‘΄μ±μ λ§λ€μ΄λΈλ€.

# Singleton Pattern μ μ¬μ©νλ©΄ μλλ μ΄μ κ° λ¬΄μμΈμ§??

<br><br><br>

# μ°Έμ‘°
- [Apple Document](https://developer.apple.com/documentation/swift/cocoa_design_patterns/managing_a_shared_resource_using_a_singleton)
