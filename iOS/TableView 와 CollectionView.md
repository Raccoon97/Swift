# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [TableView](https://github.com/Raccoon97/Swift/blob/main/iOS/TableView%20%EC%99%80%20CollectionView.md#tableview)
- [CollectionView](https://github.com/Raccoon97/Swift/blob/main/iOS/TableView%20%EC%99%80%20CollectionView.md#collectionview)
- [TableView μ CollectionView μ μ°¨μ΄](https://github.com/Raccoon97/Swift/blob/main/iOS/TableView%20%EC%99%80%20CollectionView.md#tableview-%EC%99%80-collectionview-%EC%9D%98-%EC%B0%A8%EC%9D%B4)


<br><br><br>

# TableView
- λ¨μΌ column μ λ°°μ΄λ row λ₯Ό μ¬μ©ν΄ λ°μ΄ν°λ₯Ό νμνλ λ·° μ΄λ€.
- λͺ©λ‘μ μ€νμΌλ§ν  λ μ¬μ©λλ©° μμ§ μ€ν¬λ‘€λ§ κ°λ₯νλ€.
- νμ΄λΈμ κ°λ³ ν­λͺ©μ κ΅¬μ±νλ cell μ UITableViewCell μ΄λ€.
- indexPath κ°μ ν΅ν΄ cell μ κ΅¬λΆνλ€.
- μΉμμ μ΄μ©ν΄ row λ₯Ό μκ°μ μΌλ‘ κ΅¬λΆν  μ μλ€.
- μ¬λ¬ row λ νλμ μΉμ μμ κ΅¬μ±λ  μ μκ³ , κ° μΉμμ ν€λμ νΈν°λ₯Ό κ°μ§ μ μλ€.
- μ¬μ©νκΈ° μν΄ datasource, delegate λ₯Ό κ΅¬νν΄μΌ νλ€. < UITableVideDataSource, UITableViewDelegate >

![lickability.com](https://user-images.githubusercontent.com/101554627/175514366-945d400f-d08e-4eab-adcb-d5b46ea13c1a.png)

<br><br><br>

# CollectionView
- μ¬λ¬ λ°μ΄ν°λ₯Ό κ΄λ¦¬νκ³  μ»€μ€ν κ°λ₯ν λ μ΄μμμ μ¬μ©ν΄μ μ¬μ©μμκ² λ³΄μ¬μ€ μ μλ κ°μ²΄μ΄λ€.
- CollectionView λ TableView μμ ν  μ μλ λͺ¨λ  κ²μ ν  μ μλ€.
- μΉμμ κ°μ§ μ μκ³  indexPath κ°μ ν΅ν΄ cell μ κ΅¬λΆνλ€.
- CollectionView μ κ°λ³ ν­λͺ©μ κ΅¬μ±νλ cell μ UICollectionCell μ΄λ€.
- μ¬μ©νκΈ° μν΄ datasource, delegate λ₯Ό κ΅¬νν΄μΌ νλ€. < UICollectionViewDataSource, UICollectionViewDelegate >

![lickability.com](https://user-images.githubusercontent.com/101554627/175514958-95e02ce1-3332-4992-b8fc-8a9ee96956b0.png)


<br><br><br>

# TableView μ CollectionView μ μ°¨μ΄

||TableView|CollectionView|
|------|---|---|
|μ€ν¬λ‘€|μμ§|μμ§/μν|
|μ€νμΌ|κΈ°λ³Έ μ κ³΅ μμ|κΈ°λ³Έ μ κ³΅ μμ|
|νν|1μ°¨μ|2μ°¨μ|

<br>

## TableView
- νλμ column μ μ¬λ¬ row cell μ νννλ λ°©μμ΄κΈ°μ, cell μ λͺ¨μμ ν­μ column μ λ§μΆ° λμμΈ ν΄μΌ νλ€.
- μμ§μΌλ‘λ§ μ€ν¬λ‘€μ΄ κ°λ₯νλ€.
- κΈ°λ³ΈμΌλ‘ μ κ³΅λλ μ€νμΌμ΄ μ‘΄μ¬νλ€.
- 1μ°¨μμ ννλ‘ λ¦¬μ€νΈλ₯Ό λ³΄μ¬μ€λ€.

<br>

## CollectionView
- TableView μμμ row λΌλ μ©μ΄κ° item μΌλ‘ μ¬μ©λλ€.
- row, column λͺ¨λ λ§λ€ μ μκΈ° λλ¬Έμ cell μ λͺ¨μμ μμ λ‘­κ² λμμΈν  μ μλ€.
- μμ§/μν μ€ν¬λ‘€μ΄ κ°λ₯νλ€.
- κΈ°λ³ΈμΌλ‘ μ κ³΅λλ μ€νμΌμ΄ μ‘΄μ¬νμ§ μλλ€.
- 2μ°¨μμ ννλ‘ λ¦¬μ€νΈλ₯Ό λ³΄μ¬μ€λ€.
- cell μ΄ grid ννμ΄λ€.
- UICollectionView λΌλ cell λ μ΄μμ μ€μ νλ λΆλΆμ΄ μ‘΄μ¬νλ€.



<br><br><br>

# μ°Έμ‘°
- [nareunhagaeλ](https://nareunhagae.tistory.com/19)
- [κΉμ£Όν¬λ](http://labs.brandi.co.kr/2018/05/02/kimjh.html)
