# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [JSON ( JavaScript Object Notation )](https://github.com/Raccoon97/Swift/blob/main/Etc/JSON%EA%B3%BC%20XML.md#json--javascript-object-notation-)
  - [JSON λ¬Έλ²](https://github.com/Raccoon97/Swift/blob/main/Etc/JSON%EA%B3%BC%20XML.md#json-%EB%AC%B8%EB%B2%95)
- [XML ( eXtensible Markup Language )](https://github.com/Raccoon97/Swift/blob/main/Etc/JSON%EA%B3%BC%20XML.md#xml--extensible-markup-language-)
  - [XML λ¬Έλ²](https://github.com/Raccoon97/Swift/blob/main/Etc/JSON%EA%B3%BC%20XML.md#xml-%EB%AC%B8%EB%B2%95)
- [JSON κ³Ό XML μ κ³΅ν΅μ ](https://github.com/Raccoon97/Swift/blob/main/Etc/JSON%EA%B3%BC%20XML.md#json-%EA%B3%BC-xml-%EC%9D%98-%EA%B3%B5%ED%86%B5%EC%A0%90)
- [JSON κ³Ό XML μ μ°¨μ΄μ ](https://github.com/Raccoon97/Swift/blob/main/Etc/JSON%EA%B3%BC%20XML.md#json-%EA%B3%BC-xml-%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90)


<br><br><br>

# JSON ( JavaScript Object Notation )
- λ°μ΄ν°λ₯Ό μ μ₯νκ±°λ μ μ‘ν  λ μ¬μ©λλ κ²½λμ DATA κ΅ν νμμ΄λ€.
- JSON μ μ¬λκ³Ό κΈ°κ³ λͺ¨λ μ΄ν΄νκΈ° μ½κ³  μ©λμ΄ μλ€.
- λ¨μν λ°μ΄ν°λ₯Ό νμνλ λ°©λ²μ΄λ€.
- μλ²μ ν΄λΌμ΄μΈνΈ κ°μ κ΅λ₯μμ μΌλ°μ μΌλ‘ λ§μ΄ μ¬μ©λλ€.
- λλΆλΆμ νλ‘κ·Έλλ° μΈμ΄μμ JSON ν¬λ§·μ λ°μ΄ν°λ₯Ό νΈλ€λ§ν  μ μλ€.

<br><br>

## JSON λ¬Έλ²
```json
{
  "City": [
  {
    "name": "Seoul",
    "location": "Korea"
  },
  {
    "name": "Busan",
    "location": "Korea"
  }
  ]
  
  "alphabet" : [ "Aa","Bb", "Cc", "Dd" ....]
}
```

<br><br><br>

# XML ( eXtensible Markup Language )
- λ€λ₯Έ λͺ©μ μ λ§ν¬μ μΈμ΄λ₯Ό λ§λλ λ° μ¬μ©λλ λ€λͺ©μ  λ§ν¬μ μΈμ΄μ΄λ€.
- λ€λ₯Έ μμ€νλΌλ¦¬ λ€μν μ’λ₯μ λ°μ΄ν°λ₯Ό μμ½κ² κ΅νν  μ μλλ‘ ν΄μ€λ€.
- μλ‘μ΄ νκ·Έλ₯Ό λ§λ€μ΄ μΆκ°ν΄λ κ³μ λμνλ―λ‘, νμ₯μ±μ΄ μ’λ€.
- λ°μ΄ν°λ₯Ό λ³΄μ¬μ£Όμ§ μκ³ , λ°μ΄ν°λ₯Ό μ λ¬νκ³  μ μ₯νλ κ²μ λͺ©μ μΌλ‘ νλ€.
- νμ€νΈ λ°μ΄ν° νμμ μΈμ΄λ‘ μ λμ½λ λ¬Έμλ‘λ§ μ΄λ£¨μ΄μ§λ€.

<br><br>

## XML λ¬Έλ²

```xml
<City>
  <name>Seoul</name>
  <location>Korea</location>
</City>
<City>
  <name>Busan</name>
  <location>Korea</location>
</City>
<alphabet>
  <Aa>Aa</Aa>
  <Bb>Bb</Bb>
  <Cc>Cc</Cc>
  <Dd>Dd</Dd>
  .....
</alphabet>
```

<br><br><br>

# JSON κ³Ό XML μ κ³΅ν΅μ 
- λ°μ΄ν°λ₯Ό μ μ₯νκ³  μ λ¬νκΈ° μν΄ κ³ μλμλ€.
- κΈ°κ³ λΏ μλλΌ μ¬λλ μ½κ² μ½μ μ μλ€.
- κ³μΈ΅μ μΈ λ°μ΄ν° κ΅¬μ‘°λ₯Ό κ°μ§λ€.
- λλΆλΆμ νλ‘κ·Έλλ© μΈμ΄μ μν΄ νμ±λ  μ μλ€.

<br><br><br>

# JSON κ³Ό XML μ μ°¨μ΄μ 
- JSON μ μ’λ£ νκ·Έλ₯Ό μ¬μ©νμ§ μλλ€.
- JSON μ κ΅¬λ¬Έμ΄ XML μ κ΅¬λ¬Έλ³΄λ€ ν¨μ¬ μ§§λ€.
- JSON λ°μ΄ν°κ° XML λ°μ΄ν°λ³΄λ€ λ λΉ¨λ¦¬ μ½κ³  μΈ μ μλ€.
- XML μ λ°°μ΄μ μ¬μ©ν  μ μμ§λ§ JSON μ λ°°μ΄μ μ¬μ©ν  μ μλ€.

<br><br><br>

# μ°Έμ‘°
- [κ³°λμ΄λ](https://helloworld-88.tistory.com/67)
- [TCPSchool](http://www.tcpschool.com/json/json_intro_xml)
