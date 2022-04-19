```dart
"ტრანზაქციის" შექმნა map -ით

var _questions = [
	{
		'questionText': 'What\'s your favorite color?',
		'answers': [
			{'text': 'red', 'score': 10},
			{'text': 'green', 'score': 5},
			{'text': 'blue', 'score': 1}
		],
	},
	{
		'questionText': 'What\'s your favorite movie?',
		'answers': [
			{'text': 'movie1', 'score': 10},
			{'text': 'movie2', 'score': 5},
			{'text': 'movie3', 'score': 1}
		],
	},
	{
		'questionText': 'What\'s your favorite Animal?',
		'answers': [
			{'text': 'cat', 'score': 10},
			{'text': 'dog', 'score': 5},
			{'text': 'lion', 'score': 1}
		],
	},
];


"ტრანზაქციის" შექმნა class -ით

class Transaction {
	String id;
	String title;
	double amount;
	DateTime date;  // built-in class
  
Transaction({
	required this.id,
	required this.title,
	required this.amount,
	required this.date,
});

}

-------------
// Transaction class viyenebt rogorc tips,romelic eubneba dart-s rom es cvladi(transactions) sheicavs Transaction-ebis lists
final List<Transaction> transactions = [ 
	Transaction(
		id: 'id1',
		title: 't1',
		amount: 1,
		date: DateTime.now(), // built-in class DateTime. now() <-- constructor 
                              // offered by DateTime. builds new DateTime object
	),
];
```