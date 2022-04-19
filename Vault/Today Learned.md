- Android is default operating system flutter targets,because flutter is developed by google.
- in fluttercan only have one root widget. with different leaves.to check : Platform.isIOS so return iOS sub-tree/widget, or Android sub-tree/widget.

```dart
Container(
	decoration: BoxDecoration(
		color: Color.fromRGBO(220, 220, 220, 1),  <--- Color.
	),
)
```

```dart
double get totalSpending {
	return groupedTransactionValues.fold(0.0, (sum, item) {    <--- .fold()
		return sum + (item['amount'] as double);
	});
}
```

```dart
children: groupedTransactionValues.map((data) {
	return ChartBar(
		data['day'] as String,
		data['amount'] as double,
		totalSpending == 0.0      <--- ternary operator when passing argument
			? 0.0
			: (data['amount'] as double) / totalSpending,
	);
}).toList(),
```

```dart
FittedBox(child: Text('\$${spendingAmount.toStringAsFixed(0)}')),
```

```dart
var s1 = MySingleton();

var s2 = MySingleton();

print(identical(s1, s2)); // true

print(s1 == s2);

  

print('--' * 10);
```



roca abstract classis extends aketeb aucileblad unda gadmoitano imis funqciebi, ar aris aucilebeli propertebi.

roca abstract classis implements aketeb unda gamoditano imisi funqciebic da propertebic.

```dart
String encode(String input) {
	// var output = '';
	final output = StringBuffer();
	for (final codePoint in input.codeUnits) {
		output.writeCharCode(codePoint + 1);
		// output += String.fromCharCode(codePoint + 1);
	}
	return output.toString();
}
```

```dart
class User {
	String name = 'john';
}

class anotherClass extends User {}
  
extension on User {
	void test() {
	print('testing');
}
}

var user = User();
user.test();

var another = anotherClass();
another.test();
```

```dart
Future<String> callAsyncFunc() async {
	var val = await printMe();
	return 'in callAsyncFunc, returned: $val';
}
  
Future<String> printMe() {
	return Future.delayed(Duration(seconds: 2), () => 'Printed');
}

Future<void> main() async {
	print(await callAsyncFunc());
	print('after');
}
```

```dart
final dates = List.unmodifiable([DateTime.now()]); //list.unmodifiables gareshe cashlis
dates.removeAt(0);
print(dates);
```


tu numberi gvaqvs magalitadn num x = 2, an int x = 2,   print(x.toDouble()) <--- works
magram String x = '20'.   x.toDouble()  x.toInt()  x as int <--- ar mushaobs 
amitom: 
double.parse(x) <---



```dart
List<Map<String, dynamic>> list= [
    {"name": "Shoes", "price": 100},
    {"name": "Pants", "price": 50},
  ];

  // from low to high according to price
  list.sort((a, b) => ["price"].compareTo(b["price"]));
  

  // from high to low according to price
  list.sort((a, b) => b["price"].compareTo(a["price"]));


```

```dart
List<Map<String, Object>> get groupedTransactionValues {
	return List.generate(7, (index) {
		final weekDay = DateTime.now().subtract(
		// Duration(days: index), //imdgidan dacyeba ra dgec aris
		Duration(days: DateTime.now().weekday - index), //kviridan dacyeba
		// Duration(days: (DateTime.now().weekday - 1) - index), //orshabatidan dacyeba
		);
		var totalSum = 0.0;
	  
		for (var i = 0; i < recentTransactions.length; i++) {
			if (recentTransactions[i].date.day == weekDay.day &&
			//recentTransactions[i].date.weekday == weekDay.weekday <-------
			recentTransactions[i].date.month == weekDay.month &&
			recentTransactions[i].date.year == weekDay.year) {
				totalSum += recentTransactions[i].amount;
			}
		}
  
	return {
		'day': DateFormat.E().format(weekDay).substring(0, 1),
		'amount': totalSum,
	};
});
}

------------------

print(DateTime.now().subtract(Duration(days: 1)).day); <--- ricxvi, ra ricxvi iyo
print(DateTime.now().subtract(Duration(days: 1)).weekday); <-- kviris dge(ricxvi)


```