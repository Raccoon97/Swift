# đ    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   đ 
- [Frame](https://github.com/Raccoon97/Swift/blob/main/iOS/Frame%20%EA%B3%BC%20Bounds.md#frame)
  - [frame.origin](https://github.com/Raccoon97/Swift/blob/main/iOS/Frame%20%EA%B3%BC%20Bounds.md#frameorigin)
  - [frame.size](https://github.com/Raccoon97/Swift/blob/main/iOS/Frame%20%EA%B3%BC%20Bounds.md#framesize)
  - [transformation frame.origin/ frame.size](https://github.com/Raccoon97/Swift/blob/main/iOS/Frame%20%EA%B3%BC%20Bounds.md#transformation-frameorigin-framesize)
  - [frame.origin ě ëłę˛˝](https://github.com/Raccoon97/Swift/blob/main/iOS/Frame%20%EA%B3%BC%20Bounds.md#frameorigin-%EC%9D%98-%EB%B3%80%EA%B2%BD)
- [Bounds](https://github.com/Raccoon97/Swift/blob/main/iOS/Frame%20%EA%B3%BC%20Bounds.md#bounds)
  - [bounds.origin](https://github.com/Raccoon97/Swift/blob/main/iOS/Frame%20%EA%B3%BC%20Bounds.md#boundsorigin)
  - [bounds.size](https://github.com/Raccoon97/Swift/blob/main/iOS/Frame%20%EA%B3%BC%20Bounds.md#boundssize)
  - [transformation bounds.origin/ bounds.size](https://github.com/Raccoon97/Swift/blob/main/iOS/Frame%20%EA%B3%BC%20Bounds.md#transformation-boundsorigin-boundssize)
  - [bounds.origin ě ëłę˛˝](https://github.com/Raccoon97/Swift/blob/main/iOS/Frame%20%EA%B3%BC%20Bounds.md#boundsorigin-%EC%9D%98-%EB%B3%80%EA%B2%BD)


<br><br><br>

# Frame
```swift
var frame: CGRect { get set }
```
- Super View ě˘íęłěě View ě ěěšě íŹę¸°ëĽź ëíë¸ë¤. < Super View ě ěě ( 0, 0 ) ěě ěźë§ë ë¨ě´ě ¸ ěëě§ >
  - Super View - í´ëš View ě ě ęłě¸ľ View ëĽź ë§íë¤.
- View ě ěěšë íŹę¸°ëĽź ě¤ě í  ë ěŹěŠíë¤.
- View ę° íě ëěě ë ę°ě ě ěë ěŹę°íě´ë¤.
- --> UIView ě ěěš ë° íŹę¸°ëĽź ě¤ě í  ë ěŹěŠíë¤.

<br>

- origin - Super View ě ě˘íęł
- size - View ěě­ě ëŞ¨ë ę°ě¸ë ěŹę°í

<br>

## frame.origin

<img width="1440" alt="ááłááłááľáŤááŁáş 2022-06-24 ááŠááŽ 8 47 40" src="https://user-images.githubusercontent.com/101554627/175528301-d64be4ff-c2de-4a08-9440-9e8dd7e7a8f4.png">

- View 3ę°ëĽź ë§ë  ë¤ frame.origin ě ěśë Ľíě ë ë¤ěęłź ę°ě ę˛°ęłźëĽź íě¸í  ě ěë¤.
  - FirstView ë RootView ě´ëŻëĄ ( 0.0, 0.0 )
  - SecondView ě SuperView ë FirestView ě´ëŻëĄ ( 53.0, 75.0 )
  - ThirdView ě SuperView ë SecondView ě´ëŻëĄ ( 34.0, 309.0 )
  
<br>

## frame.size

<img width="1440" alt="ááłááłááľáŤááŁáş 2022-06-24 ááŠááŽ 8 53 29" src="https://user-images.githubusercontent.com/101554627/175529061-62df48a6-f607-4385-b3f4-ed5dd3376d07.png">

- ëí frame.size ëĽź ěśë Ľíě ë ę¸° ě¤ě ë View ě width, height ëĽź ęˇ¸ëëĄ ěśë Ľíë ę˛ě ëłź ě ěë¤.

<br>

## transformation frame.origin/ frame.size

<img width="1440" alt="ááłááłááľáŤááŁáş 2022-06-24 ááŠááŽ 9 00 42" src="https://user-images.githubusercontent.com/101554627/175530115-b4f81a36-6606-4ed0-a408-f3120b090b16.png">

- íě§ë§ View ę° íě íę˛ ëëŠ´ frame.origin ęłź frame.size ę° ë°ëę˛ ëë¤.
- frame.size ë View ę° ě°¨ě§íë ěě­ě ëŞ¨ë ę°ě¸ë ěŹę°íě¸ë°, íě í  ę˛˝ě° ě°¨ě§íë ěě­ě´ ëłíëę¸° ëëŹ¸ě´ë¤.
- frame.size ę° ëłę˛˝ëëŠ´ origin ę°ë ë°ë ě ěë¤.

>- secondeView --> secondView

## frame.origin ě ëłę˛˝

<img width="1440" alt="ááłááłááľáŤááŁáş 2022-06-24 ááŠááŽ 9 23 36" src="https://user-images.githubusercontent.com/101554627/175534056-4287c89c-0362-4627-8a42-8042d9c80046.png">

- SecondView ě frame.origin ě ëłę˛˝í  ę˛˝ě° ThridView ë ę°ě´ ě´ëíë¤.
- í´ëš View ě frame.origin ě ëłę˛˝íëŠ´ SubView ë ę°ě´ ěě§ě¸ë¤.

<br><br><br>

# Bounds
```swift
var bounds: CGRect { get set }
```
- View ě ěěšě íŹę¸°ëĽź ěě ě ě˘íęł ěěě ëíë¸ë¤. ěŚ ěľě´ ěěą ě ěě ě ěě ě ( 0.0, 0.0 ) ěźëĄ ě´ę¸°ííë¤.
- --> View ë´ëśě ęˇ¸ëŚźě ęˇ¸ëŚ´ ë,  Scroll ě í  ë, transformation í View ě íŹę¸°ëĽź ěęł ěśě ë ëą ë´ëśě ěźëĄ ëłę˛˝íë ę˛˝ě°ě ěŹěŠíë¤.

<br>

- origin - í´ëš View ě ě˘íęł
- size - View ěě­ ěě˛´

<br>

## bounds.origin

<img width="1440" alt="ááłááłááľáŤááŁáş 2022-06-24 ááŠááŽ 9 06 38" src="https://user-images.githubusercontent.com/101554627/175530917-717ff4aa-ba48-4d5a-bc52-2031e02732cc.png">

- ěě ę°ě´ ę° View ě bounds.origin ě ěśë Ľí´ëł´ěěźë ëŞ¨ë ěę¸° ěě ě ěě ě ( 0.0, 0.0 ) ěźëĄ ě´ę¸°ííë¤.

<br>

## bounds.size

<img width="1440" alt="ááłááłááľáŤááŁáş 2022-06-24 ááŠááŽ 9 10 11" src="https://user-images.githubusercontent.com/101554627/175531409-f697ed13-cb25-4f10-83b6-af200641637d.png">

- bounds.size ëí frame.size ě ëěźíę˛ ěę¸° ěě ě width, height ëĽź ë°ííë¤.

<br>

## transformation bounds.origin/ bounds.size

<img width="1440" alt="ááłááłááľáŤááŁáş 2022-06-24 ááŠááŽ 9 12 58" src="https://user-images.githubusercontent.com/101554627/175531724-ab042f9f-eb15-4e1b-897d-199f5a006f77.png">

- íě ěí¨ ë¤ bounds.origin ęłź bounds.size ëĽź ěśë ĽíëŠ´ ëłíě§ ěëë¤.
- SuperView ëĽź ę¸°ě¤ěźëĄ íë frame ęłź ëŹëŚŹ bounds ë ěę¸° ěě ě ę¸°ě¤ěźëĄ íę¸° ëëŹ¸ě bounds.origin ęłź bounds.size ě ëłëě´ ěë¤.


## bounds.origin ě ëłę˛˝

<img width="1440" alt="ááłááłááľáŤááŁáş 2022-06-24 ááŠááŽ 9 30 16" src="https://user-images.githubusercontent.com/101554627/175536490-448de01d-0462-45e7-8253-63dcfe1f6413.png">

- bounds.origin ě ëłę˛˝ě View ëĽź í´ëš ěěšëĄ ě´ëěí¤ë ę˛ě´ ěëë¤.
- viewPort ëĽź View ě ěě˛´ ě˘íęłěě í´ëš ěěšëĄ ě´ëíë¤ë ę˛ě´ë¤.
  - viewPort ě ě
  ![image](https://user-images.githubusercontent.com/101554627/175538513-b1999d4e-9196-47fd-94a5-5990cc48fcae.png)

- ë¸ë ëęˇ¸ëźëŻ¸ ěě ě ëł´ëŠ´ ę¸°ěĄ´ View ě ěě­ě ëš¨ę° íëëŚŹę° ěłě ¸ěęł  ęˇ¸ ěëëĄ ( 50.0, 50.0 ) ë§íź ë´ë ¤ę° ëš¨ę° íëëŚŹę° ě ěŠëě´ěë¤.
- ěě ę°ě ě´ě ëĄ ě˘ě¸Ą ěëŽŹë ě´í°ě˛ëź ThirdView ě ěěšę° ëłę˛˝ë ę˛ě´ë¤.
- --> bounds.origin ě ëłę˛˝íë¤ë ę˛ě í´ëš View ě viewPort ě˘íëĽź ëłę˛˝íë ę˛ě´ë¤.

<img width="1440" alt="ááłááłááľáŤááŁáş 2022-06-24 ááŠááŽ 9 47 17" src="https://user-images.githubusercontent.com/101554627/175538907-234618de-f4ed-469f-88c7-18964327ab1a.png">

- View.clipsToBounds = true ëĽź ě ěŠí´ěŁźëŠ´ viewPort ě ěěšëĽź ěŽę˛źě ë, SubView ę° ë°ěźëĄ íě´ëě¤ë íěě ěě ě¤ë¤.

<br><br><br>
# ě°¸ęł 
- [ěë¤ë](https://babbab2.tistory.com/46?category=831129)
- [ě ěíë](https://sihyungyou.github.io/iOS-frame-bounds/)
