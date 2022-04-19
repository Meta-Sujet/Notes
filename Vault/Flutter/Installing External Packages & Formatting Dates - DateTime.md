intl package (internationalization) :
https://pub.dev/packages/intl 

go to --> pubspec.yaml
and add this: intl: ^0.17.0 in dependencies.

dependencies:
	flutter:
		sdk: flutter
	intl: ^0.17.0     // same level as flutter. indentation is very important

Now in your Dart code, you can use:
```dart
import 'package:intl/intl.dart';
```

if the package shouldn't get installed automatically, you can run: "flutter packages get"  in your terminal(in the project folder)

```dart
Text(
	DateFormat().format(tx.date),
	style: TextStyle(
		color: Colors.grey,
),

```

```dart
//add patter of the string, 2 ways: 

// pass pattern string to format date, it has its own language(search in official docs)
DateFormat('yyyy-MM-dd').format(tx.date), 
DateFormat('yyyy/MM/dd').format(tx.date), // and so on

// with special constructors. there are lots of constructors like this
DateFormat.yMMMd().format(tx.date),
```

```dart
List<Map<String, Object>> get groupedTransactionValues {
	return List.generate(7, (index) {
		final weekDay = DateTime.now().subtract(Duration(days: index));
		return {'day': DateFormat.E().format(weekDay), 'amount': 9.99};
	});
}
```