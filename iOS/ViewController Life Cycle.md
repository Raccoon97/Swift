# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [ViewController Life Cycle](https://github.com/Raccoon97/Swift/blob/main/iOS/ViewController%20Life%20Cycle.md#viewcontroller-life-cycle)
- [loadView](https://github.com/Raccoon97/Swift/blob/main/iOS/ViewController%20Life%20Cycle.md#loadview)
- [viewDidLoad](https://github.com/Raccoon97/Swift/blob/main/iOS/ViewController%20Life%20Cycle.md#viewdidload)
- [viewWillAppear](https://github.com/Raccoon97/Swift/blob/main/iOS/ViewController%20Life%20Cycle.md#viewwillappear)
- [viewDidAppear](https://github.com/Raccoon97/Swift/blob/main/iOS/ViewController%20Life%20Cycle.md#viewdidappear)
- [viewWillDisappear](https://github.com/Raccoon97/Swift/blob/main/iOS/ViewController%20Life%20Cycle.md#viewwilldisappear)
- [viewDidDisappear](https://github.com/Raccoon97/Swift/blob/main/iOS/ViewController%20Life%20Cycle.md#viewdiddisappear)


<br><br><br>

# ViewController Life Cycle
- κΈ°κΈ°μ νμλλ νλ©΄μ Life Cycle μ΄λ€.

![image](https://user-images.githubusercontent.com/101554627/175507245-2834c849-e25c-4327-bac2-86f4c33c084f.png)

<br>

## loadView
- ViewController κ° View λ₯Ό λ§λ€κ³  λ©λͺ¨λ¦¬μ μ¬λ¦¬λ μ­ν μ νλ€.
- View μ ViewController λ₯Ό λ§λ€κΈ° μν΄μ Interface Builder λ₯Ό μ¬μ©νλ€λ©΄ μ΄ λ©μλλ₯Ό override νμ§ λ§μμΌ νλ€. ??

<br>

## viewDidLoad
- View μ Controller κ° λ©λͺ¨λ¦¬μ λ‘λλ μν
- ViewController Life Cycle μμ νλ²λ§ νΈμΆλλ€.
- μΌλ°μ μΌλ‘ λ¦¬μμ€λ₯Ό μ΄κΈ°ννκ±°λ μ΄κΈ° νλ©΄μ κ΅¬μ±νλ μ©λλ‘ μ¬μ©νλ€.
- νλ©΄μ ν μ viewDidLoad κ° μλ viewWillAppear κ° νΈμΆλλ€.
```swift
override func viewDidLoad() {
  super.viewDidLoad()
  // Do any additional setup after loading the view, typically from a nib.
}
```

<br>

## viewWillAppear
- View κ° νλ©΄μ λνλκΈ° μ§μ μ νΈμΆλλ€.
- νλ©΄μ ν μ μ²λ¦¬νλ μ©λλ‘ μ¬μ©λλ€.

![image](https://user-images.githubusercontent.com/101554627/175509360-236fcc37-7257-46cb-a0bc-63cdbace729b.png)


<br>

## viewDidAppear
- View κ° νλ©΄μ λνλ ν νΈμΆλλ€.
- νλ©΄μ μ μ©λ  μ λλ©μ΄μμ κ·Έλ €μ€λ€.

<br>

## viewWillDisappear
- νλ©΄μ ν μ μ΄λ ViewController κ° μ¬λΌμ§κΈ° μ  νΈμΆλλ€.

<br>

## viewDidDisappear
- View κ° μ¬λΌμ§ ν νΈμΆλλ€.

<br><br><br>

# μ°Έμ‘°
- [TONOλ](https://tono18.tistory.com/11)
- [Zeddλ](https://zeddios.tistory.com/43)
