```dart
// Using function
TextStyle myStyle() => TextStyle(
	color: Colors.red,
	fontSize: 30,
	height: 1,
);

// Using getter 
// geters ver gamoviyenebt/shevqmnit funqciis shignit,buildcontext -is shignit, mxolod funqciis saxit shegvidzlia gamoyeneba,rac zemot magalitshia. magalitad roca viyenebt builder-s mis shignit ver gamoviyenebt geters
TextStyle get myStyle => TextStyle(
	color: Colors.blue,
	decoration: TextDecoration.underline,
);
```

Getters are properties which are calculated dynamically.(dynamicaly calculated property)
GETTER:  is a special type of property(not a function). 
	-its a normal property but the value is calculated dynamically.
	-you always have to return something in a getter, and you use it however like a normal property.
	it's basically a mixture of propery and method.
	you create a getter by first of all defining which type of value you want to get.
	unlike in a method you don't add parentheses because a getter is like a method that can never receive any arguments.
	

```dart
String get resultPhrase {
	String resultText;
	if (resultScore <= 8) {
		resultText = 'You are awesome';
	} else if (resultScore <= 12) {
		resultText = 'pretty likable';
	} else if (resultScore <= 16) {
		resultText = 'you are strange';
	} else {
		resultText = 'you are so bad';
	}
	return resultText;
}
```

```dart
List<Map<String, Object>> get groupedTransactionValues { 
	return List.generate(7, (index) { 
		final weekDay = DateTime.now().subtract(Duration(days: index)); 
		return {'day': DateFormat.E().format(weekDay), 'amount': 9.99}; 
	}); 
}
```