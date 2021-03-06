# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [RunLoop](https://github.com/Raccoon97/Swift/blob/main/iOS/RunLoop.md#runloop)
  - [RunLoop λ₯Ό μ¬μ©νλ κ²½μ°](https://github.com/Raccoon97/Swift/blob/main/iOS/RunLoop.md#runloop-%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94-%EA%B2%BD%EC%9A%B0)
- [RunLoop μμ μμ νλ Event Source μ κ΅¬μ‘°](https://github.com/Raccoon97/Swift/blob/main/iOS/RunLoop.md#runloop-%EC%97%90%EC%84%9C-%EC%88%98%EC%8B%A0%ED%95%98%EB%8A%94-event-source-%EC%99%80-%EA%B5%AC%EC%A1%B0)
- [RunLoop λ₯Ό μ€νμν€λ λ°©λ²](https://github.com/Raccoon97/Swift/blob/main/iOS/RunLoop.md#runloop-%EB%A5%BC-%EC%8B%A4%ED%96%89%EC%8B%9C%ED%82%A4%EB%8A%94-%EB%B0%A9%EB%B2%95)
  - [RunLoop μ λͺ¨λ](https://github.com/Raccoon97/Swift/blob/main/iOS/RunLoop.md#runloop-%EC%9D%98-%EB%AA%A8%EB%93%9C)


<br><br><br>

# RunLoop
- μμΌ, νμΌ, ν€λ³΄λ, λ§μ°μ€ λ± μ΄λ²€νΈ μμ€λ₯Ό μλ ₯λ°μ μ²λ¦¬νλ€. λν Timer μ΄λ²€νΈλ μ²λ¦¬νλ€.

<br>

- λͺ¨λ  Thread λ κ°μμ RunLoop λ₯Ό κ°μ§ μ μμΌλ©° Thread μμ± μ μλμΌλ‘ μμ±λλ€.

<br>

- MainThread λ₯Ό μ μΈν λͺ¨λ  Thread μμ RunLoop λ μλμΌλ‘ μ€νλμ§ μλλ€.
  - MainThread μμλ νλ μμν¬ μ°¨μμμ μλμΌλ‘ μ€μ νκ³  μ€νλμ§λ§, μ§μ  λ§λ  Thread μμλ μ§μ  κ΄λ¦¬ν΄μ€μΌ νλ€.
  ```swift
  // νμ¬ Thread μ RunLoop λ λ€μκ³Ό κ°μ΄ μ κ·Όν  μ μλ€.
  let runLoop = RunLoop.current
  ```

<br>

- Thread-Safe νμ§ μλ€.
  - λ€λ₯Έ Thread μμ μ€νμ€μΈ RunLoop μ λ©μλλ₯Ό νΈμΆνλ©΄ μκΈ°μΉ μμ κ²°κ³Όκ° λ°μν  μ μλ€.

<br>

- RunLoop λ λ΄λΆμ μΌλ‘ λ°λ³΅ μ€νμ νμ§ μλλ€.
  - Event Source λ₯Ό μ½κ³  μ€νμ΄ λλλ©΄ λκΈ°νλ€.
  - λͺμμ μΌλ‘ λ°λ³΅λ¬Έμ ν΅ν΄ RunLoop λ₯Ό μ€νμμΌ μ£Όμ΄μΌ νλ€.

<br>

## RunLoop λ₯Ό μ¬μ©νλ κ²½μ°
- Input Source λ₯Ό ν΅ν΄ λ€λ₯Έ Thread μ ν΅μ νλ κ²½μ°

<br>

- Timer λ₯Ό μ¬μ©νλ κ²½μ°

<br>

- Perform Selector Source λ₯Ό μ¬μ©ν΄μΌ νλ κ²½μ°

<br><br><br>

# RunLoop μμ μμ νλ Event Source μ κ΅¬μ‘°
- Input Source
  - λ€λ₯Έ Thread λ Application μμ μ¨ λΉλκΈ° μ΄λ²€νΈ
  - νΈλ€λ¬μ λΉλκΈ° μ΄λ²€νΈλ₯Ό μ λ¬νκ³  runUtilDate λ©μλκ° μ’λ£λλ€.
- Timer
  - μμ½λ μκ° λλ λ°λ³΅ κ°κ²©μΌλ‘ λ°μνλ λκΈ° μ΄λ²€νΈ
  - νΈλ€λ¬μ μ΄λ²€νΈλ₯Ό μ λ¬νμ§λ§ RunLoop λ₯Ό μ’λ£νμ§λ μλλ€.

- RunLoop λ λμμ λν΄ λΈν°νΌμΌμ΄μμ μμ±νλ€.
- λ±λ‘λ RunLoop μ΅μ λ²λ₯Ό ν΅ν΄ μλ¦Όμ μμ νκ³  μΆκ° μ²λ¦¬λ₯Ό μν΄ Thread μ κ΅¬ννλ κ²μ΄ κ°λ₯νλ€.

<p align="center">
  <img width="569" alt="img1" src="https://user-images.githubusercontent.com/101554627/178672201-ecca75bd-237e-4665-95e7-3373a4052b46.png">
</p>

<br><br><br>

# RunLoop λ₯Ό μ€νμν€λ λ°©λ²
- run()
  - run λ©μλλ₯Ό μ€ννκΈ° μ  μ μν΄ λμλ Input Source, Timer λ μκ΅¬μ μΌλ‘ μ²λ¦¬νλ€.
  - run λ©μλ μ μ Timer μ νμ Timer λ₯Ό μ€νν λͺ¨μ΅ 

<p align="center">
  <img width="569" alt="img1" src="https://user-images.githubusercontent.com/101554627/178679960-a60b02f0-7fd7-4b49-84c7-433f04e4c3c8.gif">
</p>

<br>

- run(mode: before:)
  - Loop λ₯Ό ν λ² μ€ννλλ°, ν΄λΉ λͺ¨λλ‘ μ§μ λ κΈ°κ°κΉμ§ Input μ λ§λλ€. 
<br>

- run(until: )
  - λ©μλλ₯Ό μ€ννκΈ° μ  μ μν΄ λμλ Input Source, Timer λ₯Ό μ§μ λ κΈ°κ°κΉμ§ μ²λ¦¬νλ€.
  - Loop μ μ€ν μκ°μ μ§μ ν  μ μλ€.

<p align="center">
  <img width="569" alt="img1" src="https://user-images.githubusercontent.com/101554627/178682892-b64a3880-b72b-4730-babe-c707cfb38111.gif">
</p>

<br>

- acceptInput(fotMode: before:)
  - Loop λ₯Ό ν λ² μ€ννλλ°, ν΄λΉ λͺ¨λ λλ μ§μ λ λ μ§κΉμ§λ§ μλ ₯μ νμ©νλ€.

<br><br>

## RunLoop μ λͺ¨λ

|λͺ¨λ|μ΄λ¦|μ€λͺ|
|------|---|---|
|Default|RunLoop.Mode.default(Cocoa)<br/><br/>kCFRunLoopDefaultMode(Core Foundtaion)|λλΆλΆ μ°μ°μ λν κΈ°λ³Έ λͺ¨λμ΄λ€.|
|Modal|RunLoop.Mode.modalPanel(Cocoa)|Modal Panel μμ λ°μν μ΄λ²€νΈλ§ μ²λ¦¬νλ€.<br/><br/>macOS μμλ§ μ¬μ© κ°λ₯νλ€.|
|Event Tracking|RunLoop.Mode.EventTracking(Cocoa)|νΉμ  μ΄λ²€νΈ λ£¨ν μ€μ λ€λ₯Έ μ΄λ²€νΈ λ°μμ λ§μμΌ ν  λ μ¬μ©νλ€.( λ§μ°μ€ λλκΉ μ΄λ²€νΈ λ± )<br/><br/>macOS μμλ§ μ¬μ© κ°λ₯νλ€.|
|Tracking|RunLoop.Mode.tracking(Cocoa)|μ»¨νΈλ‘€μ μΆμ νκ³  μλ μν©μμ μ¬μ©νλ€.<br/><br/>iOS, tvOS μμ μ¬μ© κ°λ₯νλ€.|
|Common modes|RunLoop.Mode.common(Cocoa)<br/><br/>kCFRunLoopCommonModes(Core Foundation)|μ¬λ¬ Mode μ μ§ν©μ΄λ€.<br/><br/>μ΄ μ΅μμΌλ‘ μΆκ°λ μ΄λ²€νΈ μμ€λ μ΅μ λ²λ common λͺ¨λμ μν λͺ¨λ  λͺ¨λμ μνκ² λλ€.<br/><br/>κΈ°λ³Έ κ°μΌλ‘ Cocoa λ default, modal, eventTracking/ tracking λͺ¨λκ° μνκ² λκ³ , Core Foundation μ default λͺ¨λλ§ μν΄μλ€.<br/><br/>μ¬κΈ°μ μλ‘μ΄ λͺ¨λλ₯Ό μΆκ°νλ €λ©΄ CFRunLoopAddCommonMode(::) λ©μλλ₯Ό μ¬μ©νλ©΄ λλ€. (μ κ±° κΈ°λ₯μ μλ€. )|

<br><br><br>


# μ°Έμ‘°
- [λΌμ΄λΈλ](https://jcsoohwancho.github.io/2019-09-01-%EC%8A%A4%EB%A0%88%EB%93%9C-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D(2)-RunLoop/)
- [μ μμ΄λΈλ](https://minosaekki.tistory.com/54)
- [μλ€λ](https://babbab2.tistory.com/68)
