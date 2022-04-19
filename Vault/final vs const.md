Dart-პროგრამირების ენაში არის ორი განსხვავებული ტიპის კონსტანტა,ესენია final-ი და const-ი. კონსტანტა არის ობიექტი რომლის მნიშვნელობაც(value) არის უცვლელი.
 ```dart
 var test = ['a','b'];
 test = [];
 test = ['c','d']   √
```
```dart
final test = ['a','b'];                        const test = ['a','b'];
test = [];                       X             test = [];
test = ['c','d'];                              test = ['c,'d];

test.add('c');              განსხვავება        test.add('c');   
test.remove('a');  √                        X  test.remove('a');
```
- fina & const-ში შეუძლებელია ხელახალი მნიშვნელობის(value) მინიჭება/reassign.
- თუ გვაქვს final კოლექცია(List),ამ List-ის ელემენტები(value) შეიძლება იყოს ცვალებადი. მაგ: test.add('...'); თუ ცვლადი არის final-ი, ეს არ ნიშნავს იმას რომ მისი მნიშვნელობაც(value) არის უცვლელი.
- თუ გვაქვს const List-ი მის შიგნით ელემენტები(value) უცვლელია.
```dart
var test = const['a','b'];
test.add('c'); X
test = const['c','d']; √
``` 
```dart
const list = [1,2]; 
//list-ი არის კონსტანტა(const),რაც ნიშნავს რომ მისი მნიშვნელობა [1,2] ავტომატურად არის უცვლელი(const)

var list = const[1,2];
//თუ მნიშვნელობა არის const-ი, არ ნიშნავს იმას რომ ცვლადიც არსი const-ი.ასე არ არის.

final list = [1,2];
//final list-ი არ ნიშნავს იმას რომ მნიშვნელობაც არის უცვლელი.
```
- There is no thing like final value.only final variable.

- Compailer - კომპაილერი არის ხელსაწყო რომელიც ახდენს ჩვენს მიერ დაწერილი კოდის კონვერტაციას მანქანურ კოდში(რომელიც გასაგები იქნება კომპიუტერისთვის).
- compile-time არის დროის რაღაც პერიოდი,რომლის დროსაც ჩვენს მიერ დაწერილი კოდი  გარდაიქმნება მანქანურ კოდში(ბინარულ/ორობით კოდში). და ჩვეულებრივ ეს ყველაფერი ხდება პროგრამის გაშვებამდე,ანუ runtime-მდე.ამ დროს კომპაილერი ამოწმებს ჩვენი კოდის/პროგრამის სინტაქსს,სემანტიკას და კოდის ტიპს.ანუ კომპაილერი პროგრამის გაშვების გარეშე/გაშვებამდე აღმოაჩენს შეცდომებს(errors).ხოლო run-time error-ის აღმოჩენა მოხდება პროგრამის გაშვების შემდეგ.
- run-time არის დროის რაღაც პერიოდი გაშვებასა და დასრულებას შორის.

- compile-time constant -ისთვის ანუ const-ისთვის(const variable) მნიშვნელობა(value) ცნობილი უნდა იყოს აუცილებლად  compile-time-ის დროს,ანუ პროგრამის გაშვებამდე. const ცვლადს ვერ მივანიჭებთ ისეთ მნიშვნელობას რომლის კალკულაციაც ხდება run-time-ზე
- run-time constant -ისთვის ანუ final ცვლადისთვის მნიშვნელობა ცნობილი ხდება მხოლოდ მაშინ როცა პროგრამას ვუშვებთ.final-ს ვიყენებთ მაშინ როცა არ ვიცით პროგრამის გაშვების დროს (ანუ run-time-ის დროს) ცვლადს რა მნიშვნელობა ექნება. value-ს კალკულაცია მოხდება run-time -ის დროს. final-ს მნიშვნელობა ენიჭება run-time -ის დროს.შეიძლება მნიშვნელობა ბევრჯერ შეიცვალოს, მაგ: 
```dart
final hour = DateTime.now().hour; √ //const აქ არ იმუშავებს
```
- თუ ერთიდაიგივე პროგრამას/კოდს ვუშვებთ რამდენჯერმე compile-time constant-ს ანუ const-ს ექნება იგივე მნიშვნელობა(value) რამდენჯერაც არ უნდა გავუშვათ.ხოლო run-time constant-ს ანუ final-ს შეიძლება ქონდეს სხვადასხვა მნიშვნელობა.


```dart
const var x = 2; X    const int x = 2; √
final var x = 2; X    final String y = 'text'; √

const x = 1+2; √
// მაგრამ DateTime-ს ვერ მივანიჭებთ. ამ შემთხვევაშ კალკულაცია ხდება compile-time-ის დროს

int x = 2;
const y = x; X
//const ცვლადის მნიშვნელობა აუცილებლად კონსტანტა უნდა იყოს(ანუ უცვლელი).

const int x = 2;
const y = x; √
//თავიდანვე ცნობილი უნდა იყოს რომ მნიშვნელობა y-ისთვის არ შეიცვლება,ეს არ ეხება final-ს:
int x = 2;
final y = x; √

const date = '2022-01-01';   √
final date = DateTime.now(); √

const x;
x = 2;   X
//const-ის ინიციალიზაცია უნდა მოხდეს ერთ ხაზზე, ეს არ ეხება: final,var,...


void finalVar(int value) {
	final finalVariable = value; √
}
void constVar(int value) {
	const constVariable = value; X
}


int Num() {
 return 2;
}
final n1 = Num(); √
const n2 = Num(); X


final list1 = const[1,2];     //const-ს თუ წავუშლით hasCode სხვადასხვა იქნება
const list2 = [1,2];
print(list1.hashCode);
print(list2.hashCode);   // ერთიდაიგივე hashCode-ი აქვთ


final dates = List.unmodifiable([DateTime.now()]);
dates.removeAt(0); X //unmodifiable-ს გარეშე წაშლის √
```

- მთავარი წესი: პირველად სცადე const-ი, და თუ არ მუშაობს(compiler-მა დაიწყო წუწუნი) მაშინ final-ი :))))

- Type Inference - ტიპის განსაზღვრა
ყოველ ჯერზე არ არის აუცილებელი ცვლადს გავუწეროთ ტიპი, Dart-ს /  compiler-ს თვითონ შეუძლია განსაზღვროს ცვლადის ტიპი. ამ პროცესს ქვია Type Inference.
```dart
fina int x = 2;  <----->  final x = 2;  //infers int type

const x = 10; <--- type is int

var x = 10;   <-- 
x = 15;  √
x = 1.5; X
//var keyword-ი ეუბნება dart-ს რომ გამოიყენოს შესაბამის ტიპი მნიშვნელობიდან(value) გამომდინარე
```