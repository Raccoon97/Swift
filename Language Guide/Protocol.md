# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [Protocol](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#protocol)
- [Protocol λ¬Έλ²](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#protocol-%EB%AC%B8%EB%B2%95)
- [Property μκ΅¬μ¬ν­](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#property-%EC%9A%94%EA%B5%AC%EC%82%AC%ED%95%AD)
- [Method μκ΅¬μ¬ν­](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#method-%EC%9A%94%EA%B5%AC%EC%82%AC%ED%95%AD)
- [Mutating Method μκ΅¬μ¬ν­](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#mutating-method-%EC%9A%94%EA%B5%AC%EC%82%AC%ED%95%AD)
- [μ΄λμλΌμ΄μ  μκ΅¬μ¬ν­](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#%EC%9D%B4%EB%8B%88%EC%85%9C%EB%9D%BC%EC%9D%B4%EC%A0%80-%EC%9A%94%EA%B5%AC%EC%82%AC%ED%95%AD)
>- [Class μμ Protocol νμ μ΄λμλΌμ΄μ μ κ΅¬ν](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#class-%EC%97%90%EC%84%9C-protocol-%ED%95%84%EC%88%98-%EC%9D%B4%EB%8B%88%EC%85%9C%EB%9D%BC%EC%9D%B4%EC%A0%80%EC%9D%98-%EA%B5%AC%ED%98%84)
>- [Failable μ΄λμλΌμ΄μ  μκ΅¬μ¬ν­](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#failable-%EC%9D%B4%EB%8B%88%EC%85%9C%EB%9D%BC%EC%9D%B4%EC%A0%80-%EC%9A%94%EA%B5%AC%EC%82%AC%ED%95%AD)
- [νμμΌλ‘μ¨μ Protocol](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#%ED%83%80%EC%9E%85%EC%9C%BC%EB%A1%9C%EC%8D%A8%EC%9D%98-protocol)
- [Delegation](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#delegation)
- [Extension μ μ΄μ©ν΄ Protocol λ°λ₯΄κ² νκΈ°](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#extension-%EC%9D%84-%EC%9D%B4%EC%9A%A9%ED%95%B4-protocol-%EB%94%B0%EB%A5%B4%EA%B2%8C-%ED%95%98%EA%B8%B0)
>- [μ‘°κ±΄μ μΌλ‘ Protocol μ λ°λ₯΄κΈ°](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#%EC%A1%B0%EA%B1%B4%EC%A0%81%EC%9C%BC%EB%A1%9C-protocol-%EC%9D%84-%EB%94%B0%EB%A5%B4%EA%B8%B0)
>- [Extension μ μ΄μ©ν΄ Protocol μ¬μ© μ μΈνκΈ°](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#extension-%EC%9D%84-%EC%9D%B4%EC%9A%A9%ED%95%B4-protocol-%EC%82%AC%EC%9A%A9-%EC%84%A0%EC%96%B8%ED%95%98%EA%B8%B0)
- [Protocol νμ μ½λ μ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#protocol-%ED%83%80%EC%9E%85-%EC%BD%9C%EB%A0%89%EC%85%98)
- [Property μμ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#property-%EC%83%81%EC%86%8D)
- [Protocol ν©μ±](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#protocol-%ED%95%A9%EC%84%B1)
- [Protocol Conform νμΈ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#protocol-conform-%ED%99%95%EC%9D%B8)
- [Optional Protocol μκ΅¬μ‘°κ±΄](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#optional-protocol-%EC%9A%94%EA%B5%AC%EC%A1%B0%EA%B1%B4)
- [Protocol Extension](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#protocol-extension)
>- [κΈ°λ³Έ κ΅¬ν μ κ³΅](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#%EA%B8%B0%EB%B3%B8-%EA%B5%AC%ED%98%84-%EC%A0%9C%EA%B3%B5)
>- [Protocol Extension μ μ μ½ μΆκ°](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/Protocol.md#protocol-extension-%EC%97%90-%EC%A0%9C%EC%95%BD-%EC%B6%94%EA%B0%80)

<br><br><br>

# Protocol
- Protocol μ νΉμ  κΈ°λ₯ μνμ νμμ μΈ μμλ₯Ό μ μν μ²­μ¬μ§μ΄λ€.
- Protocol μ λ§μ‘±μν€λ νμμ Protocol μ λ°λ₯Έλ€κ³  νλ€.
- Protocol μ κΈ°λ₯μ μΆκ°νκΈ° μν΄ Extension νλ κ²μ΄ κ°λ₯νλ€.

<br><br><br>

# Protocol λ¬Έλ²
- Protocol μ μ μλ Class, Struct, Enum λ±κ³Ό μ μ¬νλ€.
```swift
protocol SomeProtocol {
  // protocol definition goes here
}
```
- Protocol μ λ°λ₯΄λ νμμ μλμ κ°μ΄ μμ±νλ€.
```swift
struct SomeStructure: FirstProtocol, AnotherProtocol {
  // structure definition goes here
}
```
- μλΈν΄λμ±μΈ κ²½μ° μνΌν΄λμ€λ₯Ό λ§¨ μμ μ μ΄μ€λ€.
```swift
class SomeClass: SomeSuperClass, FirstProtocol, AnotherProtocol {
  // class definition goes here
}
```

<br><br><br>

# Property μκ΅¬μ¬ν­
- Protocol μμλ Property κ° Stored Property μΈμ§ Computed Property μΈμ§ λͺννμ§ μλ€.
- Property μ μ΄λ¦κ³Ό νμ, Gettable, Settable νμ§λ λͺμνλ©°, νμ Property λ ν­μ var ν€μλλ‘ μ μΈν΄μΌ νλ€.
```swift
protocol SomeProtocol {
  var mustBeSettable: Int { get set }
  var doesNotNeedToBeSettable: Int { get }
}
```
- νμμ κ°λ Property λ static ν€μλλ‘ μ μΈν΄μΌ νλ€.
```swift
protocol AnotherProtocol {
  static var someTypeProperty: Int { get set }
}
```
- μλ μ½λλ νλμ Property λ₯Ό κ°λ Protocol μ μ μΈνκ³  Stored Property μ Computed Property λ‘ μ¬μ©νλ μμμ΄λ€.
```swift
protocol FullyNamed {
  var fullName: String { get }
}

// Stored Property λ‘ μ¬μ©νκΈ° μν Struct
struct Person: FullyNamed {
  var fullName: String
}
let john = Person(fullName: "John Appleseed") // john.fullName == "John Appleseed"

// Computed Property λ‘ μ¬μ©νκΈ° μν Class
class Starship: FullyNamed {
  var prefix: String?
  var name: String
  init(name: String, prefix: String? = nil) {
    self.name = name
    self.prefix = prefix
  }
  var fullName: String {
    return (prefix != nil ? prefix! + " " : "") + name
  }
}
var ncc1701 = Starship(name: "Enterprise", prefix: "USS") // ncc1701.fullName == "USS Enterprise"
```

<br><br><br>

# Method μκ΅¬μ¬ν­
- Protocol μμλ Method λ₯Ό λͺμν  μ μλ€.
- Method νλΌλ―Έν°μ κΈ°λ³Έ κ°μ Protocol μμμ μ¬μ©ν  μ μλ€.
```swift
protocol SomeProtocol {
  static func someTypeMethod()
  func someInstanceMethod()
}
```
- μλ μ½λλ Protocol μμ νμ Method λ₯Ό λͺμνκ³  κ·Έ Protocol μ λ°λ₯΄λ ν΄λμ€μμ Method λ₯Ό κ΅¬ννλ μμμ΄λ€.
```swift
protocol RandomNumberGenerator {
  func random() -> Double
} // νμ Method μ§μ μ ν¨μλͺκ³Ό λ°νκ°μ μ§μ ν  μ μκ³ , κ΅¬νμ μ¬μ©λλ κ΄νΈλ μ μ§ μμλ λλ€.

class LinearCongruentialGenerator: RandomNumberGenerator {
  var lastRandom = 42.0
  let m = 139968.0
  let a = 3877.0
  let c = 29573.0
  // ------------------------- Protocol μ Method κ΅¬νλΆ
  func random() -> Double {
      lastRandom = ((lastRandom * a + c).truncatingRemainder(dividingBy:m))
      return lastRandom / m
  }
  // ------------------------- Protocol μ Method κ΅¬νλΆ
}
let generator = LinearCongruentialGenerator()
print("Here's a random number: \(generator.random())") // "Here's a random number: 0.3746499199817101"
print("And another one: \(generator.random())") // "And another one: 0.729023776863283"
```
- μλ μ½λλ Protocol μμ νμ Method λ₯Ό λͺμνκ³  κ·Έ Protocol μ λ°λ₯΄λ ν΄λμ€μμ νμ Method λ₯Ό κ΅¬ννμ§ μμμ λ λ°μνλ μλ¬ μμμ΄λ€.
```swift
protocol someProtocol {
  func yesConform() -> Double
}

class someClass: someProtocol { // Error : Type 'someClass' does not conform to protocol 'someProtocol'
  func noConform() -> Double {
    return 0.0
  }
}
```

<br><br><br>

# Mutating Method μκ΅¬μ¬ν­
- mutating ν€μλλ κ°νμ μλ§ μ¬μ©νλ€.
- Protocol μ mutating μ λͺμν κ²½μ° μ΄ Protocol μ λ°λ₯΄λ Class λ₯Ό κ΅¬νν  λμλ Method μ mutating μ λͺμνμ§ μμλ λλ€.
>- Struct λ Enum μ λν΄μλ mutating μ λͺμν΄μΌ ν¨.
- μλ μ½λλ mutating Method λ₯Ό μ μΈν Protocol μ μ¬μ© μμμ΄λ€.
```swift
protocol Togglable {
  mutating func toggle()
}

enum OnOffSwitch: Togglable {
  case off, on
  mutating func toggle() {
    switch self {
    case .off:
      self = .on
    case .on:
      self = .off
    }
  }
}
```

<br><br><br>

# μ΄λμλΌμ΄μ  μκ΅¬μ¬ν­
- Protocol μμ νμλ‘ κ΅¬νν΄μΌνλ μ΄λμλΌμ΄μ λ₯Ό μ§μ ν  μ μλ€.
```swift
protocol SomeProtocol {
  init(someParameter: Int)
}
```

<br>

### Class μμ Protocol νμ μ΄λμλΌμ΄μ μ κ΅¬ν
- Protocol μμ νΉμ  μ΄λμλΌμ΄μ κ° νμνλ€κ³  λͺμνκΈ° λλ¬Έμ Protocol μ λ°λ₯΄λ Class μ κ΅¬νμμ ν΄λΉ μ΄λμλΌμ΄μ μ required ν€μλλ₯Ό λΆμ¬μ€μΌ νλ€.
- Class νμμμ final λ‘ μ μΈλ κ²μλ required λ₯Ό νμνμ§ μμλ λλ€, final λ‘ μ μΈλλ©΄ μλΈν΄λμ± λμ§ μκΈ° λλ¬Έμ΄λ€.
>- μλΈν΄λμ± : λΆλͺ¨λ‘ λΆν° μ±κ²©μ μμλ°κ³  μκΈ° μμ  κ³ μ μ νΉμ±λ μΆκ°ν  μ μλ€.
>- Protocol μ μΈλΆμμλ μ΄λμλΌμ΄μ  μμ final ν€μλλ₯Ό μ¬μ©ν  μ μλ€.
```swift
class SomeClass: SomeProtocol {
  required init(someParemeter: Int) {
      // initializer implementation goes here
  }
    
}

final class SomeFinalClass: SomeProtocol {
  init(someParemeter: Int) {
      // initializer implementation goes here
  }
}
```
- νΉμ  Protocol μ νμ μ΄λμλΌμ΄μ λ₯Ό κ΅¬ννκ³ , SuperClass μ μ΄λμλΌμ΄μ λ₯Ό μλΈν΄λμ± νλ κ²½μ° μ΄λμλΌμ΄μ  μμ required ν€μλμ override ν€μλλ₯Ό λΆμ¬μ€λ€.
```swift
protocol SomeProtocol {
  init()
}

class SomeSuperClass {
  init() {
    // initializer implementation goes here
  }
}

class SomeSubClass: SomeSuperClass, SomeProtocol { 
  // required --> SomeProtocol Conformance, override --> SomeSuperClass SubClassing
  required override init() {
    // initializer implementation goes here
  }
}
```

<br>

### Failable μ΄λμλΌμ΄μ  μκ΅¬μ¬ν­
- Protocol μ Failable ν μ΄λμλΌμ΄μ λ₯Ό μ μΈν  μ μλ€.
- Failable μ΄λμλΌμ΄μ  : Class, Struct, Enum μμ μ΄κΈ°νλ₯Ό νλ€κ° μ€ν¨νλ κ²½μ°κ° μμ μ μλ€λ©΄ μ μνλ μ΄λμλΌμ΄μ .
>- Optional Type μ²λΌ init λ€μ ? λ₯Ό λΆμ¬μ£Όλ©΄ λλ€.
```swift
// Failable μ΄λμλΌμ΄μ μ μμ
struct Animal { 
  let species: String 
  init?(species: String) { 
    if species.isEmpty { 
      return nil 
    } 
    self.species = species 
  } 
}
```
- Failable μ΄λμλΌμ΄μ λ₯Ό Protocol μμ μ¬μ©νλ λ²
```swift
protocol Something {
  init?()
}

struct Some: Something {
  init() {
  }
}
```

<br><br><br>

# νμμΌλ‘μ¨μ Protocol
- Protocol λ νλμ νμμΌλ‘ μ¬μ©λλ―λ‘ λ€μκ³Ό κ°μ μν©μμ Protocol μ μ¬μ©ν  μ μλ€.
>- Func, Method, μ΄λμλΌμ΄μ μ νλΌλ―Έν° νμ νΉμ λ¦¬ν΄ νμ
>- let, var, Property μ νμ
>- μ»¨νμ΄λμΈ Array, Dictionary λ±μ μμ΄ν νμ
- Protocol μ νμμ΄κΈ° λλ¬Έμ μ²« κΈμλ₯Ό λλ¬Έμλ‘ μ μ΄μ€λ€.
- μλ μ½λλ Protocol μ νμμΌλ‘ μ¬μ©ν μμμ΄λ€.
```swift
protocol RandomNumberGenerator {
  func random() -> Double
}

class LinearCongruentialGenerator: RandomNumberGenerator {
  var lastRandom = 42.0
  let m = 139968.0
  let a = 3877.0
  let c = 29573.0
  func random() -> Double {
    lastRandom = ((lastRandom * a + c).truncatingRemainder(dividingBy:m))
    return lastRandom / m
  }
}

class Dice {
  let sides: Int
  let generator: RandomNumberGenerator
  init(sides: Int, generator: RandomNumberGenerator) {
    self.sides = sides
    self.generator = generator
  }
  func roll() -> Int {
    return Int(generator.random() * Double(sides)) + 1
  }
}

var d6 = Dice(sides: 6, generator: LinearCongruentialGenerator())
for _ in 1...5 {
  print("Random dice roll is \(d6.roll())")
}

"""
    RandomNumberGenerator λ₯Ό generator μμμ νμμΌλ‘ κ·Έλ¦¬κ³  μ΄λμλΌμ΄μ μ νλΌλ―Έν° νμΌλ‘ μ¬μ©νλ€.
    Diceλ₯Ό μ΄κΈ°ν ν  λ generator νλΌλ―Έν° λΆλΆμ RandomNumberGenerator Protocol μ λ°λ₯΄λ μΈμ€ν΄μ€λ₯Ό λ£μ΅λλ€.
"""
```

<br><br><br>

# Delegation
- Delegation μ Class νΉμ Strutc μΈμ€ν΄μ€μ νΉμ  νμμ λν μ±μμ λκΈΈ μ μκ² ν΄μ£Όλ λμμΈ ν¨ν΄ μ€ νλμ΄λ€.
```swift
protocol DiceGame {
  var dice: Dice { get }
  func play()
}
protocol DiceGameDelegate: AnyObject {
  func gameDidStart(_ game: DiceGame)
  func game(_ game: DiceGame, didStartNewTurnWithDiceRoll diceRoll: Int)
  func gameDidEnd(_ game: DiceGame)
}
```
- DiceGame Protocol μ μ μΈνκ³  DiceGameDelegated μ μ μΈν΄μ μ€μ  DiceGame μ νμμ κ΄λ ¨λ κ΅¬νμ DiceGameDelegate λ₯Ό λ°λ₯΄λ μΈμ€ν΄μ€μ μμνλ€.
- DiceGameDelegate λ₯Ό AnyObject λ‘ μ μΈνλ©΄ Class λ§ μ΄ Protocol μ λ°λ₯Ό μ μκ² νλ€.
```swift
class SnakesAndLadders: DiceGame {
  let finalSquare = 25
  let dice = Dice(sides: 6, generator: LinearCongruentialGenerator())
  var square = 0
  var board: [Int]
  init() {
    board = Array(repeating: 0, count: finalSquare + 1)
    board[03] = +08; board[06] = +11; board[09] = +09; board[10] = +02
    board[14] = -10; board[19] = -11; board[22] = -02; board[24] = -08
  }
  weak var delegate: DiceGameDelegate?
  func play() {
    square = 0
    delegate?.gameDidStart(self)
    gameLoop: while square != finalSquare {
      let diceRoll = dice.roll()
      delegate?.game(self, didStartNewTurnWithDiceRoll: diceRoll)
      switch square + diceRoll {
      case finalSquare:
        break gameLoop
      case let newSquare where newSquare > finalSquare:
        continue gameLoop
      default:
        square += diceRoll
        square += board[square]
        }
      }
    delegate?.gameDidEnd(self)
  }
}
```
- SnakesAndLadders λ DiceGame Protocol μ λ°λ₯Έλ€.
- DiceGameDelegate Protocol μ λ°λ₯΄λ Delegate 'delegate' λ₯Ό κ°λλ€.
- κ²μμ μ€ννμ λ delegate?.gameDidStart(self), delegate?.game(self, didStartNewTurnWithDiceRoll: diceRoll), delegate?.gameDidEnd(self)λ₯Ό μ€ννλ€.
- delegateλ κ²μμ μ§νμν€λλ° λ°λμ νμν κ±΄ μλλΌμ μ΅μλλ‘ μ μλμ΄ μλ€.
- μλ μ½λλ DiceGameDelegate λ₯Ό μμνλ delegate DiceGameTracker λ₯Ό κ΅¬νν μμμ΄λ€.
```swift
class DiceGameTracker: DiceGameDelegate {
  var numberOfTurns = 0
  func gameDidStart(_ game: DiceGame) {
    numberOfTurns = 0
    if game is SnakesAndLadders {
      print("Started a new game of Snakes and Ladders")
    }
    print("The game is using a \(game.dice.sides)-sided dice")
  }
  func game(_ game: DiceGame, didStartNewTurnWithDiceRoll diceRoll: Int) {
    numberOfTurns += 1
    print("Rolled a \(diceRoll)")
  }
  func gameDidEnd(_ game: DiceGame) {
    print("The game lasted for \(numberOfTurns) turns")
  }
}
```
- DiceGameTracker λ₯Ό μ΄μ©ν΄μ κ²μμ μ§νμν¨λ€. κ²μμΌ tracking κ΄λ ¨λ μμμ DiceGameTracker κ° μμ λ°μ κ·Έ κ³³μμ μ«νλλ€.
```swift
let tracker = DiceGameTracker()
let game = SnakesAndLadders()
game.delegate = tracker
game.play()
// Started a new game of Snakes and Ladders
// The game is using a 6-sided dice
// Rolled a 3
// Rolled a 5
// Rolled a 4
// Rolled a 5
// The game lasted for 4 turns
```

<br><br><br>

# Extension μ μ΄μ©ν΄ Protocol λ°λ₯΄κ² νκΈ°
- μ΄λ―Έ μ‘΄μ¬νλ νμμ Protocol μ λ°λ₯΄κ² νκΈ° μν΄ Extension μ μ¬μ©ν  μ μλ€.
- μλ κ°μ μ κ·Ό κΆνμ΄ μμ΄λ Extension μ νμ©ν΄ κΈ°λ₯μ νμ₯ν  μ μλ€.
>- μ΄λ―Έ Extension μΌλ‘ νμ₯λ νμμ Extension μ μΆκ°νλ©΄ κ·Έ νμμ μΆκ°λ κΈ°λ₯μ μ¬μ©ν  μ μλ€.
```swift
protocol TextRepresentable {
  var textualDescription: String { get }
}

extension Dice: TextRepresentable {
  var textualDescription: String {
    return "A \(sides)-sided dice"
  }
}

let d12 = Dice(sides: 12, generator: LinearCongruentialGenerator())
print(d12.textualDescription) // "A 12-sided dice"
```

<br>

### μ‘°κ±΄μ μΌλ‘ Protocol μ λ°λ₯΄κΈ°
- νΉμ  μ‘°κ±΄μ λ§μ‘±μν¬ λλ§ Protocol μ λ°λ₯΄λλ‘ μ νν  μ μλ€.
- where ν€μλλ₯Ό μ΄μ©ν΄ μ μνλ€.
- μλ μ½λλ TextRepresentableμ λ°λ₯΄λ Arrayμ€μ Arrayμ κ° μμκ° TextRepresentableμΈ κ²½μ°μλ§ λ°λ₯΄λ νλ‘ν μ½μ μ μνλ€.
```swift
extension Array: TextRepresentable where Element: TextRepresentable {
  var textualDescription: String {
    let itemsAsText = self.map { $0.textualDescription }
    return "[" + itemsAsText.joined(separator: ", ") + "]"
  }
}
let myDice = [d6, d12]
print(myDice.textualDescription) // "[A 6-sided dice, A 12-sided dice]"

// Array μ κ° μμκ° TextRepresentable μ λ°λ₯΄κΈ° λλ¬Έμ textualDecription Property λ₯Ό μ¬μ©ν  μ μλ€.
// textualDescriptionλ Arrayμ λͺ¨λ  μμ΄νμ μννκ³  κ°κ°μ textualDescriptionλ₯Ό κ²°ν©ν΄ λ°ννλ Method μ΄λ€.
```

### Extension μ μ΄μ©ν΄ Protocol μ¬μ© μ μΈνκΈ°
- μ΄λ€ Protocol μ μ¬μ©νλ λͺ¨λ  μ‘°κ±΄μ λ§μ‘±νμ§λ§ μμ§ κ·Έ Protocol μ λ°λ₯Έλ€λ μ μΈμ νμ§ μμλ€λ©΄, λΉ Extension μΌλ‘ μ μΈν  μ μλ€.
- μλ μ½λλ Protocol μ λ°λ₯Έλ€λ μ μΈμ Extension μ νκ³  Protocol μ λ°λ₯΄κΈ° μν κ΅¬νμ Struct μ κ΅¬νν΄ μ¬μ©νλ μμμ΄λ€.
```swift
struct Hamster {
  var name: String
  var textualDescription: String {
    return "A hamster named \(name)"
  }
}
extension Hamster: TextRepresentable { }

let simonTheHamster = Hamster(name: "Simon")
let somthingTextRepresentable: TextRepresentable = simonTheHamster
print(somethingTextRepresentable.textualDescription) // "A hamster named Simon"
```
- Protocol μ μκ΅¬μ¬ν­μ κΈ°μ νλ κ²λ§μΌλ‘ Protocol μ μ¬μ© μ‘°κ±΄μ μΆ©μ‘±μν¬ μ μλ€.
- λ°λμ μ΄λ€ Protocol μ λ°λ₯΄λμ§ κΈ°μ ν΄μΌ νλ€.

<br><br><br>

# Protocol νμ μ½λ μ
- Protocol μ Array, Dictionary λ± μ½λ μ νμμ λ£κΈ° μν νμμΌλ‘ μ¬μ©ν  μ μλ€.
- μλ μ½λλ Protocol μ λ°λ₯΄λ Array μ μ¬μ© μμμ΄λ€.
```swift
let things: [TextRepresentable] = [game, d12, simonTheHamster]
// λͺ¨λ  κ°μ²΄λ TextRepresentable μ λ°λ₯΄λ―λ‘ textualDescription Propety λ₯Ό κ°λλ€.

for things in things {
  print(thing.textualDescription)
}
// A game of Snakes and Ladders with 25 squares
// A 12-sided dice
// A hamster named Simon
```

<br><br><br>

# Property μμ
- Class μμμ²λΌ Protocol λ μμν  μ μλ€.
- μ¬λ¬ Protocol μ μμλ°λ κ²½μ° μ½€λ§(,) λ‘ κ΅¬λΆνλ€.
```swift
protocol InheritingProtocol: SomeProtocol, AnotherProtocol {
  // protocol definition goes here
}
```
- μλ μ½λλ TextRepresentable Protocol μ μμλ°μ μλ‘μ΄ Protocol PrettyRepresentable μ κ΅¬ννμ¬ μ¬μ©νλ μμμ΄λ€.
```swift
protocol PrettyTextRepresentable: TextRepresentable {
  var prettyTextualDescription: String { get }
}

extension SnakesAndLadders: PrettyTextRepresentable {
  var prettyTextualDescription: String {
    var output = textualDescription + ":\n"
    for index in 1...finalSquare {
      switch board[index] {
      case let ladder where ladder > 0:
        output += "β² "
      case let snake where snake < 0:
        output += "βΌ "
      default:
        output += "β "
      }
    }
    return output
  }
}

print(game.prettyTextualDescription)
// A game of Snakes and Ladders with 25 squares:
// β β β² β β β² β β β² β² β β β βΌ β β β β βΌ β β βΌ β βΌ β
```

<br><br><br>

# Protocol ν©μ±
- λμμ μ¬λ¬ Protocol μ λ°λ₯΄λ νμμ μ μΈν  μ μλ€. 
- μλ μ½λλ λμμ μ¬λ¬ Protocol μ λ°λ₯΄λ λ°©λ²μ μμμ΄λ€.
```swift
protocol Named {
  var name: String { get }
}
protocol Aged {
  var age: Int { get }
}

// λμμ Named, Aged Protocol μ λ°λ₯΄λ Struct μ΄λ€.
struct Person: Named, Aged {
  var name: String
  var age: Int
}
func wishHappyBirthday(to celebrator: Named & Aged) {
  print("Happy birthday, \(celebrator.name), you're \(celebrator.age)!")
}
let birthdayPerson = Person(name: "Malcolm", age: 21)
wishHappyBirthday(to: birthdayPerson) //  "Happy birthday, Malcolm, you're 21!"


// Location νλ‘ν μ½κ³Ό μμNamed νλ‘ν μ½μ λ°λ₯΄λ City ν΄λμ€μ κ΅¬ν
class Location {
  var latitude: Double
  var longitude: Double
  init(latitude: Double, longitude: Double) {
    self.latitude = latitude
    self.longitude = longitude
  }
}
class City: Location, Named {
  var name: String
  init(name: String, latitude: Double, longitude: Double) {
    self.name = name
    super.init(latitude: latitude, longitude: longitude)
  }
}
func beginConcert(in location: Location & Named) {
  print("Hello, \(location.name)!")
}

let seattle = City(name: "Seattle", latitude: 47.6, longitude: -122.3)
beginConcert(in: seattle)
// Prints "Hello, Seattle!"
```
<br><br><br>

# Protocol Conform νμΈ
- μ΄λ€ νμμ΄ νΉμ  Protocol μ λ°λ₯΄λμ§ λ€μκ³Ό κ°μ λ°©λ²μΌλ‘ νμΈν  μ μλ€.
- is λ₯Ό μ΄μ©νμ¬ μ΄λ€ νμμ΄ νΉμ  Protocol μ λ°λ₯΄λμ§ νμΈ κ°λ₯νλ€. λ°λ₯΄λ©΄ true/ λ°λ₯΄μ§ μμΌλ©΄ false λ°ν
- as? λ νΉμ  Protocol μ λ°λ₯΄λ κ²½μ° κ·Έ Optional νμμ Protocol νμμΌλ‘ λ€μ΄μΊμ€νΈλ₯Ό νκ² λκ³  λ°λ₯΄μ§ μλ κ²½μ° nil μ λ°ννλ€.
- as! λ κ°μ λ‘ νΉμ  Protocol μ λ°λ₯΄λλ‘ μ μνλ€. λ€μ΄μΊμ€νΈμ μ€ν¨νλ©΄ λ°νμ μλ¬κ° λ°μνλ€.
- μλ μ½λλ as? νμΈ λ°©λ²μ μμμ΄λ€.
```swift
// area λΌλ κ°μ νμλ‘ νλ HasArea Protocol μ μ μΈνλ€.
protocol HasArea {
    var area: Double { get }
}

// HasArea Protocol μ λ°λ₯΄λ Circle, Country Class λ₯Ό μ μΈνλ€.
class Circle: HasArea { // Computed Property κ΅¬ν
  let pi = 3.1415927
  var radius: Double
  var area: Double { return pi radius radius }
  init(radius: Double) { self.radius = radius }
}
class Country: HasArea {
  var area: Double  // Stored Property κ΅¬ν
  init(area: Double) { self.area = area }
}

// HasArea Protocol μ λ°λ₯΄μ§ μλ Animal Class λ₯Ό μ μΈνλ€.
class Animal {
  var legs: Int
  init(legs: Int) { self.legs = legs }
}

// Circle, Country, Animal μ μΈμ€ν΄μ€λ₯Ό objects Array μ λ£λλ€.
let objects: [AnyObject] = [
  Circle(radius: 2.0),
  Country(area: 243_610),
  Animal(legs: 4)
]

// Array λ₯Ό μννλ©° as? HasArea κ΅¬λ¬Έμ μ¬μ©ν΄ Protocol μ λ°λ₯΄λμ§ νμΈν ν λ°λ₯΄λ κ²½μ° HasArea νμμΌλ‘ λ€μ΄μΊμ€ν νλ€.
  // λ€μ΄μΊμ€ν - λΆλͺ¨ν΄λμ€μ νμμ μμν΄λμ€μ νμμΌλ‘ λ€μ΄νμ¬ μΊμ€ννλ€ 
for object in objects {
  if let objectWithArea = object as? HasArea {
      print("Area is \(objectWithArea.area)")
  } else {
      print("Something that doesn't have an area")
  }
}
// Circle, Country μΈμ€ν΄μ€λ HasArea λ₯Ό λ°λ₯΄κΈ° λλ¬Έμ area κ°μ΄ λ°νλκ³ , Animal μΈμ€ν΄μ€λ else μ μ΄ μ€νλλ€.
// Area is 12.5663708
// Area is 243610.0
// Something that doesn't have an area
```

<br><br><br>

# Optional Protocol μκ΅¬μ‘°κ±΄
- Protocol μ μ μΈνλ©΄μ νμ κ΅¬νμ΄ μλ Optional κ΅¬ν μ‘°κ±΄μ μ μν  μ μλ€.
- μ΄ Protocol μ μ μλ₯Ό μν΄ @objc ν€μλλ₯Ό Protocol μμ λΆμ΄κ³ , κ°λ³ Func, Property μλ @objc μ Optional ν€μλλ₯Ό λΆμΈλ€.
- @objc Protocol μ Class νμμμλ§ μ¬μ©ν  μ μκ³ , Struct, Enum μμλ μ¬μ©ν  μ μλ€.
- μλ μ½λλ λ κ°μ§ Optional κ΅¬νμ ν  μ μλ Protocol μ μμμ΄λ€.
```swift
@objc protocol CounterDataSource {
    @objc optional func increment(forCount count: Int) -> Int
    @objc optional var fixedIncrement: Int { get }
}

// Counter Class μμ CounterDataSource λ₯Ό λ°λ₯΄λ dataSource λ₯Ό μ μΈ
class Counter {
    var count = 0
    var dataSource: CounterDataSource?
    func increment() {
        if let amount = dataSource?.increment?(forCount: count) {
            count += amount
        } else if let amount = dataSource?.fixedIncrement {
            count += amount
        }
        // increment?(forCount: count), fixedIncrement λ Optional μ΄λ―λ‘ κ΅¬νμ΄ μλμ΄μ΄ μμ μ μκΈ° λλ¬Έμ Optional Chaining μ μ΄μ©ν΄ νμΈν΄λ³Έλ€.
    }
}

// CounterDataSource Protocol μ λ°λ₯΄λ ThreeSource Class λ₯Ό μ μΈνλ€.
class ThreeSource: NSObject, CounterDataSource {
    let fixedIncrement = 3
}

// Counter μΈμ€ν΄μ€μ dataSource λ₯Ό ThreeSource λ‘ λΆν° μλ ₯λ°μ κ°μ μ¦κ°μν¬ μ μλ€.
var counter = Counter()
counter.dataSource = ThreeSource()
for _ in 1...4 {
    counter.increment()
    print(counter.count)
}
// 3
// 6
// 9
// 12

// λ³΅μ‘ν μμ λ‘ CounterDataSource λ₯Ό μ΄μ©ν΄ μ΄λ€ κ°μ 0μ μλ ΄νλλ‘ λ§λλ ν΄λμ€λ₯Ό μ μΈνλ€.
class TowardsZeroSource: NSObject, CounterDataSource {
    func increment(forCount count: Int) -> Int {
        if count == 0 {
            return 0
        } else if count < 0 {
            return 1
        } else {
            return -1
        }
    }
}

// -4 λΆν° μμνμ§λ§ TowardZeroSource μ increment μ μν΄ counter.increment() κ° νΈμΆλ  λ λ§λ€ 0μ κ°κΉμμ§λ©΄μ κ²°κ΅­ 0μ μλ ΄νλ€.
counter.count = -4
counter.dataSource = TowardsZeroSource()
for _ in 1...5 {
    counter.increment()
    print(counter.count)
}
// -3
// -2
// -1
// 0
// 0
```

<br><br><br>

# Protocol Extension
- Extension μ μ΄μ©ν΄ Protocol μ νμ₯ν  μ μλ€.
- Extension μ μ΄μ©ν΄ κ΅¬νμ μΆκ°ν  μ μμ΄λ λ€λ₯Έ Protocol λ‘ νμ₯/ μμν  μλ μμΌλ©° κ·Έλ κ² νλ €λ©΄ Protocol μμ²΄μ κ΅¬νν΄μΌ νλ€.
- μλ μ½λλ RandomNumberGenerator μ randomBool() μ μΆκ°νμ¬ μ¬μ©νλ μμμ΄λ€.
```swift
extension RandomNumberGenerator {
  func randomBool() -> Bool {
    return random() > 0.5
  }
}

// μλ μ½λμ κ°μ΄ generator.random(), generator.randomBool() λ λ€ μ΄μ©ν  μ μλ€.
let generator = LinearCongruentialGenerator()
print("Here's a random number: \(generator.random())") // "Here's a random number: 0.3746499199817101"
print("And here's a random Boolean: \(generator.randomBool())") // "And here's a random Boolean: true"
```

<br>

### κΈ°λ³Έ κ΅¬ν μ κ³΅
- Extension μ κΈ°λ³Έ κ΅¬νμ μ κ³΅νλλ° μ¬μ©ν  μ μλ€.
- νΉμ  Protocol μ λ°λ₯΄λ νμ μ€μμ κ·Έ Protocol μ μκ΅¬μ¬ν­μ λν΄ μμ²΄μ μΌλ‘ κ΅¬ννκ² μμΌλ©΄ κ·Έκ²μ μ¬μ©νκ³  μλλ©΄ κΈ°λ³Έ κ΅¬νμ μ¬μ©νλ€.
- Protocol μμ²΄μμλ μ μΈλ§ κ°λ₯νλ°, Extension μ μ΄μ©ν΄ κΈ°λ³Έ κ΅¬νμ μ κ³΅ν  μ μλ€.
- μλ μ½λλ PrettyTextRepresentable Protocol μμ prettyTextualDescription Property λ₯Ό textualDescription λ₯Ό λ°ννλλ‘ κ΅¬νν μμμ΄λ€.
```swift
extension PrettyTextRepresentable {
  var prettyTextualDescription: String {
    return textualDescription
  }
}
```

<br>

### Protocol Extension μ μ μ½ μΆκ°
- Protocol Extension μ΄ νΉμ  μ‘°κ±΄μμλ§ μ μ©λλλ‘ μ μΈν  μ μλ€.
- μμ νΉμ  μ‘°κ±΄μμλ§ λ°λ₯΄κ² νκΈ°λμ λ€λ₯Έ λ΄μ©μ΄μ§λ§ λκ°μ΄ where ν€μλλ₯Ό μ¬μ©νλ€.
- μλ μ½λλ Collection μ Element κ° Equatable μΈ κ²½μ°μλ§ μ μ©λλ allEqual() Method λ₯Ό κ΅¬νν μμμ΄λ€.
```swift
extension Collection where Element: Equatable {
  func allEqual() -> Bool {
    for element in self {
      if element != self.first {
        return false
      }
    }
    return true
  }
}

let equalNumbers = [100, 100, 100, 100, 100]
let differentNumbers = [100, 100, 200, 100, 200]

print(equalNumbers.allEqual()) // "true"
print(differentNumbers.allEqual()) // "false"

```

<br><br><br>

μ°Έμ‘°
- [Swift Document](https://docs.swift.org/swift-book/LanguageGuide/Protocols.html)
