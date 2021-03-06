# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [Type Casting](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Type%20Casting.md#type-casting)
- [Type Casting μ μν ν΄λμ€ κ³μΈ΅κ΅¬μ‘° μ μΈ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Type%20Casting.md#type-casting-%EC%9D%84-%EC%9C%84%ED%95%9C-%ED%81%B4%EB%9E%98%EC%8A%A4-%EA%B3%84%EC%B8%B5%EA%B5%AC%EC%A1%B0-%EC%84%A0%EC%96%B8)
- [Type νμΈ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Type%20Casting.md#type-%ED%99%95%EC%9D%B8)
- [Downcasting](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Type%20Casting.md#downcasting)
- [Any, AnyObject μ Type Casting](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Type%20Casting.md#any-anyobject-%EC%9D%98-type-casting)

<br><br><br>

# Type Casting
- μΈμ€ν΄μ€μ νμμ νμΈνκ±°λ μΈμ€ν΄μ€λ₯Ό κ°μ κ³μΈ΅μ μλ superclass λλ subclass λ‘ μ·¨κΈνλ λ°©λ²μ΄λ€.
- Type Casting μλ is μ as λ μ°μ°μλ₯Ό μ¬μ©νλ€.
- Type Casting μ μ΄μ©νλ©΄ νΉμ  νλ‘ν μ½μ λ°λ₯΄λμ§ νμΈν  μ μλ€.
- Casting μ μ€μ  μΈμ€ν΄μ€λ κ°μ λ°κΎΈλ κ²μ΄ μλλΌ μ§μ ν νμμΌλ‘ μ·¨κΈνλ κ²μ΄λ€.
- Upcasting -> subclass μ μΈμ€ν΄μ€λ₯Ό superclass μ Type μΌλ‘ μ°Έμ‘°νλ€.
>- Upcasting μ ν­μ μ±κ³΅νλ©°, μ§μ  νμμ λͺμν΄μ μ¬μ©ν  μ μκ³ , as μ°μ°μλ₯Ό μ¬μ©ν΄μ ν  μλ μλ€.
- Downcasting -> superclass μΈμ€ν΄μ€λ₯Ό subclass μ Type μΌλ‘ μ°Έμ‘°νλ€.
>- Upcasting λ μΈμ€ν΄μ€λ₯Ό λ€μ μλ subclass Type μΌλ‘ μ°Έμ‘°ν  λ μ¬μ©νλ€.
>- Downcasting μ μ€ν¨ν  μ μκΈ° λλ¬Έμ as?, as! μ°μ°μλ₯Ό μ¬μ©νλ€.

<br><br><br>

# Type Casting μ μν ν΄λμ€ κ³μΈ΅κ΅¬μ‘° μ μΈ
- Type Casting λμμ νμΈνκΈ° μν ν΄λμ€
```swift
class MediaItem {
  var name: String
  init(name: String) {
    self.name = name
  }
}
```
- μμ MediaItem ν΄λμ€λ₯Ό μλΈν΄λμ±ν΄μ λ κ°μ λ€λ₯Έ μλΈν΄λμ€λ₯Ό λ§λ€κ³  κ·Έ λ ν΄λμ€λ₯Ό μμ΄νμΌλ‘ κ°λ λ°°μ΄μ μ μΈ
```swift
class Movie: MediaItem {
  var director: String
  init(name: String, director: String) {
    self.director = director
    super.init(name: name)
  }
}

class Song: MediaItem {
  var artist: String
  init(name: String, artist: String){
    self.artist = artist
    super.init(name: name)
  }
}

let library = [
  Movie(name: "Casablanca", director: "Michael Curtiz"),
  Song(name: "Blue Suede Shoes", artist: "Elvis Presley"),
  Movie(name: "Citizen Kane", director: "Orson Welles"),
  Song(name: "The One And Only", artist: "Chesney Hawkes"),
  Song(name: "Never Gonna Give You Up", artist: "Rick Astley")
]
```
- μμ μ½λμμ library λ°°μ΄μ΄ κ°κ³  μλ Movie, Song μΈμ€ν΄μ€μ κ³΅ν΅ λΆλͺ¨λ MediaItem μ΄κΈ° λλ¬Έμ library λ°°μ΄μ νμ μΆλ‘ μ μν΄ [MediaItem] λ°°μ΄μ νμ κ°κ² λλ€.
- library λ°°μ΄μ μννλ©΄ Movie, Song νμμ΄ μλλΌ MediaItem νμμ΄λΌλ κ²μ νμΈν  μ μλ€.
- νμ μ§μ μ μν΄μλ downcasting μ μ¬μ©ν΄μΌ νλ€.

<br><br><br>

# Type νμΈ
- is μ°μ°μλ₯Ό μ΄μ©ν΄ νΉμ  μΈμ€ν΄μ€μ νμμ νμΈν  μ μλ€. 
- μλ μμλ λ°°μ΄μ μννκ³  μμ΄νμ΄ νΉμ  νμμΌ λ λ§λ€ μ«μλ₯Ό μ¦κ°νλ μ½λμ΄λ€.
```swift
var movieCount = 0
var songCount = 0

for item in library {
  if item is Movie {
    movieCount += 1
  } else if item is Song {
    songCount += 1
  }
}

print("Media library contains \(movieCount) movies and \(songCount) songs")
// "Media library contains 2 movies and 3 songs"
```

<br><br><br>

# Downcasting
- νΉμ  ν΄λμ€ νμμ μμλ λ³μλ νΉμ  μλΈν΄λμ€μ μΈμ€ν΄μ€λ₯Ό μ°Έμ‘°νκ³  μμ μ μλ€.
- as? μ as! μ°μ°μλ₯Ό μ΄μ©ν΄ μ΄λ€ νμμ μΈμ€ν΄μ€μΈμ§ νμΈν  μ μλ€.
- as? λ νΉμ  νμμ΄ λ§λμ§ νμ ν  μ μμ λ μ¬μ©νλ€.
- as! λ νΉμ  νμμ΄ λ§λμ§ νμ ν  μ μμ λ μ¬μ©νλ€ λ¨, ν΄λΉ νμμ΄ μλλΌλ©΄ λ°νμ μλ¬κ° λ°μνλ€.
- μλ μμλ λ°°μ΄μ mediaItem μ΄ Movie λλ Song μΈμ€ν΄μ€ μΌ μ μκΈ° λλ¬Έμ λ€μ΄μΊμ€νμ μν΄ as? λ₯Ό μ¬μ©ν μ½λμ΄λ€.
```swift
for item in library {
  if let movie = item as? Movie {
    print("Movie: \(movie.name), dir. \(movie.director)")
  } else if let song = item as? Song {
    print("Song: \(song.name), by \(song.artist)")
  }
}

// Movie: Casablanca, dir. Michael Curtiz
// Song: Blue Suede Shoes, by Elvis Presley
// Movie: Citizen Kane, dir. Orson Welles
// Song: The One And Only, by Chesney Hawkes
// Song: Never Gonna Give You Up, by Rick Astley
```


<br><br><br>

# Any, AnyObject μ Type Casting
- Swift μμλ λ κ°μ§ νΉλ³ν νμμ΄ μλ€.
- Any --> ν¨μ νμμ ν¬ν¨ν λͺ¨λ  νμμ λνλΈλ€.
- AnyObject --> λͺ¨λ  ν΄λμ€ νμμ μΈμ€ν΄μ€λ₯Ό λνλΈλ€
- μλ μμλ Any νμμ as λ₯Ό μ΄μ©ν΄ Type Casting νλ μ½λμ΄λ€.
```swift
var things = [Any]()

things.append(0)
things.append(0.0)
things.append(42)
things.append(3.14159)
things.append("hello")
things.append((3.0, 5.0))
things.append(Movie(name: "Ghostbusters", director: "Ivan Reitman"))
things.append({ (name: String) -> String in "Hello, \(name)" })

for thing in things {
  switch thing {
  case 0 as Int:
    print("zero as an Int")
  case 0 as Double:
    print("zero as a Double")
  case let someInt as Int:
    print("an integer value of \(someInt)")
  case let someDouble as Double where someDouble > 0:
    print("a positive double value of \(someDouble)")
  case is Double:
    print("some other double value that I don't want to print")
  case let someString as String:
    print("a string value of \"\(someString)\"")
  case let (x, y) as (Double, Double):
    print("an (x, y) point at \(x), \(y)")
  case let movie as Movie:
    print("a movie called \(movie.name), dir. \(movie.director)")
  case let stringConverter as (String) -> String:
    print(stringConverter("Michael"))
  default:
    print("something else")
  }
}
```
- Int, Double λΏ μλλΌ Tuple, Func λν Any νμμ ν¬ν¨λ  μ μλ€λ κ²μ νμΈν  μ μλ€.
- Optional νμ λν ν¬ν¨νμ§λ§ Any νμμ μ¬μ©ν΄μΌ νλ κ³³μ Optional μ μ¬μ©νλ©΄ κ²½κ³ κ° λ°μλλ€.
```swift
let optionalNumber: Int? = 3 things.append(optionalNumber) // κ²½κ³  
things.append(optionalNumber as Any) // κ²½κ³  μμ
```
<br><br><br>

# μ°Έμ‘°
- [Apple Document](https://docs.swift.org/swift-book/LanguageGuide/TypeCasting.html)
