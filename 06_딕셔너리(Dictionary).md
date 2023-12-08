`Dictionary`는 키-값 쌍으로 데이터를 저장하는 컬렉션 타입입니다.
키는 유일해야 하며,
각 키는 하나의 값(값은 중복 가능)을 가집니다.

## 딕셔너리의 선언 및 초기화

- **빈 딕셔너리 선언**:
```Swift
var namesOfIntegers = [Int: String]() //[키: 벨류(값)]
var citiesByCountry = [String: String]()
```   
- **초기값이 있는 딕셔너리**:
```Swift
var airportCodes: [String: String] = ["ICN": "인천국제공항", "GMP": "김포국제공항"]
var phoneNumbers: [String: Int] = ["홍길동": 12345678, "이순신": 87654321]
```

## 딕셔너리에 값 추가 및 수정

- **값 추가/수정**:
```Swift
airportCodes["CJU"] = "제주국제공항"
phoneNumbers["박지성"] = 98765432
```

- **값 수정2**: 이전 값 확인할 때 유용
```Swift
if let oldValue = airportCodes.updateValue("제주국제공항", forKey: "CJU") {
	print("CJU의 이전 공항 이름은 \(oldValue)였습니다.")
}

if let oldNumber = phoneNumbers.updateValue(11223344, forKey: "이순신") {
	print("이순신의 이전 번호는 \(oldNumber)였습니다.")
}
```
## 딕셔너리에서 값 제거

- **값 제거**:
```Swift
airportCodes["PUS"] = "부산국제공항"
airportCodes["PUS"] = nil  // PUS 키와 관련된 값 제거  
phoneNumbers["김연아"] = 55566677
phoneNumbers["김연아"] = nil  // 김연아 키와 관련된 값 제거
```

## 딕셔너리의 순회

- **for-in 루프를 사용한 딕셔너리 순회**:
```Swift
for (airportCode, airportName) in airportCodes {
	print("\(airportCode): \(airportName)")
} 

for (name, number) in phoneNumbers {     
	print("\(name)의 번호는 \(number)입니다.")
}
```
## 딕셔너리의 유용한 속성과 메서드

- **딕셔너리의 크기**:
```Swift
let airportCount = airportCodes.count
let phoneNumberCount = phoneNumbers.count
```   

- **빈 딕셔너리 확인**:
```Swift
let isAirportsEmpty = airportCodes.isEmpty
let isPhoneNumbersEmpty = phoneNumbers.isEmpty
```
