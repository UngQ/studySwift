`Set`은 중복되지 않는 값의 모음을 저장하는 데 사용되는 컬렉션 타입입니다.
`set` 집합은 `array` 배열과 유사하지만, 두 가지 주요 차이점이 있습니다.
집합은 순서가 없으며, 각 요소는 유일해야 합니다.

## 집합의 선언 및 초기화

- **빈 집합 선언**:
```Swift
var letters = Set<Character>()
var numbers = Set<Int>()
```

- **초기값이 있는 집합**:
```Swift
var favoriteGenres: Set<String> = ["Rock", "Classical", "Hip hop"]
var digits: Set = [1, 2, 3, 4, 5]
```   

## 집합에 값 추가 및 삭제

- **값 추가**: `.insert`
```Swift
favoriteGenres.insert("Jazz")
digits.insert(6)
```
   
- **값 삭제**: `.remove`
```Swift
if let removedGenre = favoriteGenres.remove("Rock") {
	print("\(removedGenre) was removed.")
} 

if let removedDigit = digits.remove(1) {
	print("\(removedDigit) was removed.")
}
```

## 집합 확인

- **특정 요소가 집합에 있는지 확인**: `.contains`
```Swift
let containsRock = favoriteGenres.contains("Rock")
let containsSeven = digits.contains(7)
```
 
## 집합의 순회

- **for-in 루프를 사용한 집합 순회**:
```Swift
for genre in favoriteGenres {
	print("\(genre)")
}

for digit in digits {
	print("\(digit)")
}
```

## 집합 연산

- **집합 간의 연산 (합집합, 교집합)**:
```Swift
let evenDigits: Set = [0, 2, 4, 6, 8]
let oddDigits: Set = [1, 3, 5, 7, 9]
let primeDigits: Set = [2, 3, 5, 7]
let unionSet = evenDigits.union(oddDigits)
let intersectionSet = oddDigits.intersection(primeDigits)
```
