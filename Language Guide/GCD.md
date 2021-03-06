# π    [Go Main](https://github.com/Raccoon97/Swift/blob/main/README.md)   π 
- [GCD( Grand Central Dispatch )](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#gcd-grand-central-dispatch-)
- [GCD μ κ΅¬μ‘°](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#gcd-%EC%9D%98-%EA%B5%AC%EC%A1%B0)
  - [Dispatch Queue](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#dispatch-queue)
  - [Dispatch Group](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#dispatch-groups)
  - [Dispatch Semaphores](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#dispatch-semaphores)
  - [Dispatch WorkItem](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#dispatch-work-item)
  - [Dispatch Sources](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#dispatch-sources)
- [GCD μ μ¬μ©](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#gcd-%EC%9D%98-%EC%82%AC%EC%9A%A9)
  - [Dispatch Queue](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#dispatch-queue-1)
  - [Dispatch WorkItem](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#dispatch-workitem)
  - [Dispatch Group](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#dispatch-group)
  - [Dispatch Semaphores](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#dispatch-semaphores-1)
- [GCD μ μ₯/λ¨μ ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#gcd-%EC%9D%98-%EC%9E%A5%EB%8B%A8%EC%A0%90)
- [μ£Όμ](https://github.com/Raccoon97/Swift/blob/main/Language%20Guide/GCD.md#%EC%A3%BC%EC%9D%98)
<br><br><br>

# GCD( Grand Central Dispatch )
- <p>μ§μ μ μΌλ‘ Thread λ₯Ό κ΄λ¦¬νμ§ μκ³  μμμ Queue λ‘ λ³΄λ΄ λΆμ°μ²λ¦¬ νλ λ°©λ²</p>
- <p>iOS SDK μλ λΉλκΈ° μ²λ¦¬λ₯Ό μν NSOperation λ° NSOpercisionQueue ν΄λμ€κ° μμκ³  μ νμ λ λ€λ₯Έ λ°©λ²μΌλ‘ GCD λ₯Ό λ°ννλ€.</p>
- <p>GCD λ λ©ν°μ½μ΄ μμ€νμμ λμμ± μ€νμ μ κ³΅νλ νλ μμν¬μ΄λ€.</p>
- <p>κΈ°μ‘΄ GCD λ C λΌμ΄λΈλ¬λ¦¬ μ²λΌ μ μμ€μ APIλ‘ μ κ³΅λμ΄μ μ½κ² μ¬μ©νκΈ° μ΄λ €μ λ€.</p>
- <p>iOS 10 μ΄ν Dispatch FrameWork κ° GCD μ λͺ¨λ  λ΄μ©μ μΊ‘μν ν΄μ μ¬μ©νκΈ° μ½κ² μ¬μ©μ΄ κ°λ₯νλ€.</p>

<br><br><br>

# GCD μ κ΅¬μ‘°
### Dispatch Queue
- <p>λΉλκΈ° μ μΌλ‘ Task λ₯Ό μνμν¬ μ μλ Queue μ΄λ€.</p>
- <p>Task λ₯Ό κ΄λ¦¬νλ Queue μ΄κΈ° λλ¬Έμ, FIFO λ°μ΄ν° κ΅¬μ‘°μ΄λ€. ( First In, First Out )</p>
- Dispatch Queue μλ Serial Dispatch Queue μ Concurrent Dispatch Queue, Main Dispatch Queue κ° μλ€.
  - Serial Disaptch Queue - Queue μ μμΈ Task λ€μ μμ°¨μ μΌλ‘ 1κ°μ© μμνλ©° μ΄μ  Task κ° μ’λ£λλ©΄ λ€μ Task λ₯Ό μ€ννλ€. ( 1λ²μ 1κ° )
  - oncurrent Disaptch Queue - Queue μ μμΈ Task λ€μ μμλλ‘ μμνλ©°, μ΄μ  Task κ° μ’λ£λλ κ²μ κΈ°λ€λ¦¬μ§ μκ³  λ€μ Task λ₯Ό μ€ννλ€. ( FIFO κ΅¬μ‘°λ‘ κ³μ Task λ₯Ό μ€ν )
  - Main Dispatch Queue - Application μ MainThread μμ RunLoop λ₯Ό ν΅ν΄ κ΄λ¦¬λλ Queue μ΄λ©°, Serial νκ² μνλλ€.

<br>

- <p>Block Coding μ κΈ°λ°μΌλ‘ μ΄ν΄νκΈ° μ½λ€.</p>
- <p>μ¬μ©νκΈ° μ¬μ΄ μΈν°νμ΄μ€λ₯Ό μ κ³΅νλ€.</p>
- <p>OS μμ μλμΌλ‘ Thread ν κ΄λ¦¬λ₯Ό μννλ€.</p>
- Serial
  - μ΄μ  μμμ΄ λλλ©΄ λ€μ μμμ μμ°¨μ μΌλ‘ μ€ννλ μ§λ ¬ ννμ Queue
  - νλμ μμμ μ€ννκ³  λλ  λκΉμ§ λκΈ°μ΄μ μλ λ€λ₯Έ μμμ μ μ λ―Έλ£¬ λ€ κ·Έ μμμ΄ λλλ©΄ μ€νλλ€.

![αα‘αα?α«αα©αα³](https://user-images.githubusercontent.com/101554627/170698624-bf1951ec-5ad6-4fa4-8755-0bc552ab4379.png)
- Concurrent
  - μ΄μ  μμμ΄ λλ  λκΉμ§ κΈ°λ€λ¦¬μ§ μκ³  λ³λ ¬ ννλ‘ λμμ μ€νλλ Queue
  - λκΈ°μ΄μ μλ μμμ λμμ λ³λμ Thread λ₯Ό μ¬μ©νμ¬ μ€ννλ€.

![αα‘αα?α«αα©αα³ (1)](https://user-images.githubusercontent.com/101554627/170698649-40b37c6b-5aa4-476a-ab93-88c9c98fda75.png)

<br>

### Dispatch Groups
- <p>Dispatch Queueλ€μ Task λ€μ λͺ¨λν°λ§ νλ κ·Έλ£Ήμ΄λ€.</p>
- <p>λͺ¨λ  νλ€μ΄ λμμ μλ£νμ λ, λ€μ Taskλ₯Ό μ§νμν¬ μ μλ€.</p>

<br>

### Dispatch Semaphores
- <p>MultiThread νκ²½μμ Thread Safeλ₯Ό μ§ν€κΈ° μνμ¬ κ°μ²΄λ λ³μμ λν μ κ·Όμ lock νλ κΈ°μ‘΄μ semaphoreμ μ μ¬ν κ°λμ΄λ€.</p>

<br> 

### Dispatch Work Item
- <p>Dispatch Queue λ€μ μΊ‘μν νμ¬ μ¬μ©ν  μ μκ² ν κ², μ€κ°μ μ·¨μκ° κ°λ₯νλ€.</p>

<br>

### Dispatch Sources
- <p>νλ‘μΈμ€μ Notification,Signal λ± μ΄λ²€νΈλ₯Ό λͺ¨λν°λ§ ν  μ μκ³ , μ΄λ²€νΈκ° λ°μνλ©΄ Dispatch Queueμ Taskλ₯Ό Submit νλ€.</p>

<br><br><br>

# GCD μ μ¬μ©

### Dispatch Queue
- <p>μλμ κ°μ΄ μ Dispatch Queue λ₯Ό μ½κ² λ§λ€ μ μλ€.</p>
- <p>Debugging ν  λ Thread λͺ©λ‘μ My Dispatch Queue λΌλ λ μ΄λΈμ΄ λνλλ€.</p>
```swift
let dq = DispatchQueue(label: "my dispatch queue")
dq.async {
    print ("hello")
}
```
- <p>μ¬λ¬ κ°μ λ£¨νλ₯Ό λμμ μ€νν  μ μλ€.
```swift
// λ κ°μ λμ λ£¨ν
DispatchQueue.global().async {
    for i in 1...5 {
        print("global async \(i)")
    }
}

DispatchQueue.global().async {
    for i in 1...5 {
        print("global async 2 \(i)")
    }
}
```
- <p>.global() λ©μλλ Default global queue λ₯Ό λ°ννλ€.</p>
- <p>Async λ©μλλ Serial νμ§ μλ€. -> λμμ±</p>
- <p>Serial νκΈ°λ₯Ό μνλ©΄ sync() λ©μλλ₯Ό μ¬μ©ν΄μΌ νλ€. -> λΉλμμ±</p>
- <p>sync λ° async λ λͺ¨λ λ€λ₯Έ λ§€κ°λ³μλ₯Ό μ¬μ©νλ©° κ°μ₯ μΌλ°μ μΈ λ§€κ°λ³μλ λΈλ‘μ μ λ¬νλ κ²μ΄λ€.</p>
- <p>μλ‘ λ€λ₯Έ QoS λκΈ°μ΄μμ λΈλ‘μ μ€νν  μ μλ€.</p>
```swift
DispatchQueue.global(qos: .background).async {
    for i in 1...5 {
        print("global async \(i)")
    }
}

DispatchQueue.global(qos: .userInteractive).async {
    for i in 1...5 {
        print("global async 2 \(i)")
    }
}
```

<br>

- <p>QoS λ μ°μ  μμλ₯Ό κ²°μ νκ³  μμ€νμ΄ μ±λ₯μ μ΅μ ν ν  μ μλλ‘ μ§μνλ€.</p>

```swift
// Main Queue, λ©μΈ ν€λμ ν΄λΉνλ ν΄λμ€μ΄λ€.
DispatchQueue.global(pos: .userInteractive) {}

// μ μ κ° μμν μμ, μ μ κ° μλ΅μ κΈ°λ€λ¦Ό
// μ¬μ©μκ° νΈλ¦¬κ±°ν μμμ κΈ°λ³Έ Thred μμ μ€νν  νμκ° μλ€. 
// DISPATCH_QUEUE_PRIORITY_HIGH μ λμΌνλ€.
DispatchQueue.global(pos: .userInitiated) {}

// userInitiated μ utility μ μ€κ°
// κΈ°λ³Έ QoS μ΄λ€. 
// DISPATCH_QUE_PRIORITY_DEFAULT μ λμΌνλ€.
DispatchQueue.global(pos: .default) {}

// μκ°μ΄ κ±Έλ¦¬λ©° μ¦κ°μ μΈ μλ΅μ΄ νμνμ§ μμ κ²½μ°
// νμΌ λ° λ€νΈμν¬ I/O μ κ°μ μμ€ν λ¦¬μμ€μ μμ‘΄νλ Dispatch ν­λͺ©μ μ¬μ©λλ€. 
// DISPATCH_QUE_PRIORITY_LOW μ λμΌνλ€.
DispatchQueue.global(pos: .utility) {}

// λμ λ³΄μ΄μ§ μλ λΆλΆμ μμ, μλ£λλ μκ°μ΄ μ€μνμ§ μμ κ²½μ°
// μ°μ  μμκ° λ?μ μμμ μ¬μ©λλ€. 
// DISPATCH_QUE_PRIORITY_BACKGROUND μ λμΌνλ€. 
DispatchQueue.global(pos: .background) {}

// QoS κ° μ§μ λμ§ μλ κ²½μ°
DispatchQueue.global(pos: .unspecified) {}
```

- <p>Main Dispatch Queue λ₯Ό ν΅ν΄ μλ μμμ²λΌ Main Thread μ μμμ μ μΆν  μ μλ€.</p>
```swift
DispatchQueue.main.async {
    for i in 1...5 {
        print("main async \(i)")
    }
}
```
- <p>Main Queue μμ λκΈ°μ μΌλ‘ μμμ μ€ννλ©΄ DeadLock μ΄ κ±Έλ¦°λ€.</p>
- <p>Dispatch Queue λ₯Ό μ¬μ©νλ©΄ concurrentPerform λ©μλλ₯Ό μ¬μ©ν΄ λμ λ£¨νλ₯Ό κ°λ¨ν μνν  μ μλ€.</p>
```swift
DispatchQueue.concurrentPerform(iterations: 5) { (i) in
    print(i)
}
```

<br>

### Dispatch WorkItem
- <p>μμ ν­λͺ©μ κ°λμ μΊ‘μν ν κ²</p>
- <p>λΈλ‘μ μ¬μ©νμ¬ μΈμ€ν΄μ€λ₯Ό μ΄κΈ°ν ν ν νμ¬ Thread μμ μ€ννκ±°λ Dispatch Queue μ μ μΆν  μ μλ€.</p>
```swift
let dispatchWorkItem = DispatchWorkItem {
    for i in 1...5 {
        print("DispatchWorkItem \(i)")
    }
}
// Thread μ€ν
dispatchWorkItem.perform()

// Dispatch Queue μ μ μΆ
DispatchQueue.global().async(execute: dispatchWorkItem)
```
- <p>μ·¨μ νλκ·Έκ° μμΌλ©° Thread μμ μ€ννκΈ° μ μ μ·¨μλλ©΄ Dispatch Queue μμ μ€ννμ§ μκ³  κ±΄λλ΄λ€.</p>
- <p>μ€ν μ€μ μ·¨μλλ©΄ μ·¨μ νλ‘νΌν°κ° True λ₯Ό λ°ννλ€. μ΄ κ²½μ° μ€νμ΄ μ€λ¨λλ€.</p>

```swift
// dispatch work item μμ±
var dispatchWorkItem: DispatchWorkItem? = DispatchWorkItem {
    for i in 1...5 {
        if (dispatchWorkItem?.isCancelled)!{
            break
        }
        sleep(1)
        print("DispatchWorkItem : \(i)")
    }
}
//global queue μ μ μΆ
DispatchQueue.global().async(execute: dispatchWorkItem!)

//3μ΄ λ€μ μμ μ·¨μ
DispatchQueue.global().async{
    sleep(3)
    dispatchWorkItem?.cancel()
}
```

<br>

### Dispatch Group
- <p>Dispatch Group μ μ¬μ©νλ©΄ λ€λ₯Έ λκΈ°μ΄μμ μ€νλλ κ²½μ°μλ λ€λ₯Έ μμμ νμΈν  μ μλ€.</p>
```swift
let dispatchWorkItem = DispatchWorkItem{
    print("work item start")
    sleep(1)
    print("work item end")
}

let dg = DispatchGroup()

// Work Items λ₯Ό Group μ λ£κΈ°
let dispatchQueue = DispatchQueue(label: "custom dq")
dispatchQueue.async(group: dg) {
    print("block start")
    sleep(2)
    print("block end")
}
DispatchQueue.global().async(group: dg, execute: dispatchWorkItem)

// λͺ¨λ  Group μ΄ λλλ©΄ λ©μμ§ μΆλ ₯νκΈ°
dg.notify(queue: DispatchQueue.global()) {
    print("dispatch group over")
}
```

<br>

### Dispatch Semaphores
- <p>Semaphores λ₯Ό μ¬μ©νμ¬ μ€ν νλ¦μ μ μ΄ν  μ μλ€.</p>
```swift
let semaphore = DispatchSemaphore(value: 0)
DispatchQueue.global().async {
    print("waiting for at least one signal")
    
    // μ νΈ λκΈ°
    semaphore.wait()
    print("At least one signal has been received")
}

DispatchQueue.global().async {
    sleep(2)
    print("calling signal")
    
    // μ νΈ μ μ‘
    semaphore.signal()
}
```
- <p>wait λ©μλλ₯Ό μ¬μ©ν΄ μκ° μ΄κ³Όλ₯Ό μ§μ ν  μ μλ€.</p>
```swift
let sem = DispatchSemaphore(value: 0)
DispatchQueue.global().async {
    print("waiting for at least one signal for 1 second")
    
    // μ νΈ λκΈ°
    let res = sem.wait(timeout: DispatchTime.now() + 1)
    if(res == .timedOut){
        print("wait timed out")
    }else{
        print("At least one signal has been received")
    }
}

DispatchQueue.global().async {
    sleep(3)
    print("calling signal")
    
    // μ νΈ μ μ‘
    sem.signal()
}
```

<br><br><br>

# GCD μ μ₯/λ¨μ 
### μ₯μ 
- <p>Thread μ κ΄λ¦¬λ₯Ό κ°λ°μκ° μλ OS κ° ν΄μ£ΌκΈ° λλ¬Έμ μ κ²½μΈ μΌμ΄ μ λ€.</p>
- <p>Block μ½λ© λ°©μμΌλ‘ μ¬μ΄ κ°λ°μ΄ κ°λ₯νλ€.</p>

<br>

### λ¨μ 
- <p>Queue μ μλ Task λ€μ μ·¨μκ° κΉλ€λ‘­λ€. ( DispatchWorkItem μ μ΄μ©νλ©΄ κ°λ₯νλ€. )</p>
- <p>Block Coding μ μνμ°Έμ‘°μ μ£Όμν΄μΌ νλ€.</p>
- <p>DeadLock μ μ£Όμν΄μΌ νλ€. ( MainQueue μμμ Sync λ DeadLock μ μΌκΈ°νλ€. )</p>
- Obj-C μ Swift μ Block/Closure μμ μ°Έμ‘°νλ μΈλΆ λ³μκ° Reference Type μΈμ§ Value Type μΈμ§ κ³ λ €ν΄μΌ νλ€.
  - Obj-C Block λ΄ λ³μλ Value Type μ΄λ©° Swift Closuer λ΄ λ³μλ Reference Type μ΄λ€.
  - Ojb-C Block μ κ²½μ°λ _block ν€μλλ₯Ό μ μΈνμ¬ Reference Type μΌλ‘ μ¬μ©ν  μ μλ€.
  - Swift Clouser μ κ²½μ°λ Capture List λ₯Ό μ μΈνμ¬ Value Type μΌλ‘ μ¬μ©ν  μ μλ€.

<br><br><br>

# μ£Όμ
- <p>μ΄λ€ μμμ΄ μλ£λκ³  λμ UI λ₯Ό κ°±μ μν€λ κ²½μ°, Application μ Main Thread μμ μ²λ¦¬λλλ‘ ν΄μΌ νλ€.</p>
- <p>MainQueue λ Serial νκΈ° λλ¬Έμ, UI κ°±μ μ΄ μλ API νΈμΆμ΄λ Download κ°μ μμμ MainQueue μμ ν  κ²½μ° Freezing νμμ΄ μΌμ΄λλ©° Application μ ν¨μ¨μ΄ λ¨μ΄μ§κ² λλ€.</p>
- <p>tableView νΉμ collectionView λ₯Ό μ΄μ©ν List λ₯Ό λ³΄μ¬μ£Όλ λμμμ Image μ λν λ€μ΄λ‘λλ₯Ό MainQueue μμ λͺ¨λ μνν  κ²½μ° λ²λ²μμ΄ μΌμ΄λλ€.</p>
- <p>Image DownLoad λ globalQueue( Concurrent Queue ) μμ μνμν€κ³  Download μλ£ μ UI κ°±μ λ§ MainQueue μμ νΈμΆν΄μΌ νλ€.</p>
- <p>UI κ°±μ μ΄ νμνμ§ μκ³ , μνμκ°μ΄ κΈΈκ±°λ, μνμ μλΉλλ λ¦¬μμ€κ° ν° κ²½μ° Councurrent Queue λ₯Ό μ΄μ©νλ©΄ μ’λ€.</p>

<br><br><br>

# μ°Έμ‘°
- [Askeλ](https://burzum17.tistory.com/8)
- [Yassine Benabbasλ](https://medium.com/@yostane/swift-sweet-bits-the-dispatch-framework-ios-10-e34451d59a86)
