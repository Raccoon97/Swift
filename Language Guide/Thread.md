# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [Thread](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Thread.md#thread)
- [Thread Safe](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Thread.md#thread-safe)
- [atomic](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Thread.md#atomic)
- [non-atomic](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Thread.md#non-atomic)
- [Thread Safe λ₯Ό μν λ°©λ²](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Thread.md#thread-safe-%EB%A5%BC-%EC%9C%84%ED%95%9C-%EB%B0%A9%EB%B2%95)

<br><br><br>

# Thread
- <p>Thread λ Process λ΄μμ μ€μ λ‘ μμμ μννλ μ£Όμ²΄λ₯Ό μλ―Ένλ€.</p>
- <p>λͺ¨λ  Process μλ ν κ° μ΄μμ Thread κ° μ‘΄μ¬νμ¬ μμμ μννλ€.</p>
- <p>λ κ° μ΄μμ Thread λ₯Ό κ°μ§λ Process λ₯Ό Multi-Threaded Process λΌκ³  νλ€.</p>

<br>
  
![image](https://user-images.githubusercontent.com/101554627/170500892-a2cbc9c9-3707-402c-9f17-c80422cfbb16.png)

<br><br><br>

# Thread Safe
- <p>Thread Safe λ Multi-Threaded νλ‘κ·Έλλ°μμ μ΄λ€ ν¨μλ λ³μ, κ°μ²΄κ° μ΄λ€ Thread λ‘ λΆν° λμμ μ κ·Όμ΄ μ΄λ£¨μ΄μ Έλ λ¬Έμ κ° μκΈ°μ§ μλλ€λ κ²μ μλ―Ένλ€.</p>
- <p>iOS μμλ Multi-Threaded λ°©μμ μ¬μ©νλ€.</p>
- <p>Multi-Threaded μ κ²½μ° Stack μ μ μΈν Heap, Data μμ­ λ±μ κ³΅μ νκ³  μκΈ° λλ¬Έμ ν Thread μμ μ¬μ©μ€μΈ κ³³μ λ€λ₯Έ Thread κ° μ κ·Όνλ©΄ λ¬Έμ κ° μκΈΈ μ μλ€.</p>
- <p>Multi-Process μμλ κ³΅μ νλ μμκ³΅κ°μ΄ μκΈ° λλ¬Έμ λ¬Έμ κ° μκΈ°μ§ μλλ€.</p>

<br>

## atomic
- <p>νλ‘κ·Έλλ°μμ λ°μ΄ν°μ λ³κ²½μ΄ λμμ μΌμ΄λ κ²μ²λΌ λ³΄μ΄κ² νλ κ²</p>
- <p>atomic ν λ°μ΄ν°λ₯Ό λ³κ²½νλ λμμλ lock μ κ±Έμ΄μ λ€λ₯Έ Thread μ μ κ·Όμ΄ μ΄λ£¨μ΄μ§μ§ μκ² νλ€.</p>
- <p>Property κ° atomic νλ€λ κ²μ Multi-Threaded νκ²½μμ λ°μ΄ν°κ° μμ λλ μκ°μλ μ κ·Όν  μ μλ€λ κ²μ΄λ€.</p>
- <p>atomic Property λ ν­μ Concurrent κ° μλ serial νκ² μ κ·Όλλ€.</p>
- <p>Swift λ Thread Safe λ₯Ό κ³ λ €ν μΈμ΄κ° μλκΈ° λλ¬Έμ λͺ¨λ  Property λ non-atomic μ΄λ―λ‘ λ³λλ‘ atomic μ μ§μ νλ κ²μ΄ λΆκ°νλ€.</p>
- <p>μμ κ°μ μ΄μ λ‘ GCD( Grand Central Dispatch ) λ₯Ό ν΅ν΄ λ°μ΄ν°λ₯Ό λ€λ€μΌ νλ€.</p>

<br>

## non-atomic
- <p>λ°νλ κ°μ λν΄ λ³΄μ₯νμ§ μλλ€. μ νν κ°μ΄κ±°λ μ°λ κΈ° κ°μ΄λ€.</p>

<br>

## Thread Safe λ₯Ό μν λ°©λ²
- <p>Mutual Exclusion - Thread μ lock μ΄λ semaphore λ₯Ό κ±Έμ΄μ κ³΅μ μμμλ νλμ Thread λ§ μ κ·Ό κ°λ₯νκ² νλ€.</p>
- <p>Thread Local Storage - νΉμ  Thread μλ§ μ κ·Ό κ°λ₯ν μ μ₯μλ₯Ό λ§λ λ€.</p>
- <p>ReEntrancy - Thread μμ λμνλ μ½λκ° λμΌ Thread μμ μ¬μνλκ±°λ, λ€λ₯Έ Thread μμ ν΄λΉ μ½λλ₯Ό λμμ μνν΄λ λμΌν κ²°κ³Όλ₯Ό μ»μ μ μλλ‘ μμ±νλ€.</p>
- <p>Atomic Operation - λ°μ΄ν° λ³κ²½ μ atomic νκ² λ°μ΄ν°μ μ κ·Όνλλ‘ λ§λ λ€.</p>
- <p>Immutable Object - κ°μ²΄ μμ± μ΄νμ κ°μ λ³κ²½ν  μ μλλ‘ λ§λ λ€.</p>

<br><br><br>

# μ°Έμ‘°
- [ginjoλ](https://ginjo.tistory.com/17)
- [μ μμ΄λΈλ](https://minosaekki.tistory.com/50)
