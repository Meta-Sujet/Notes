```dart
var questions = [
	{
		'questionText': 'What\'s your favorite color?',
		'answers': ['red', 'green', 'blue', 'pink'],
	},
	{
		'questionText': 'What\'s your favorite movie?',
		'answers': ['movie1', 'movie2', 'movie3'],
	},
	{
		'questionText': 'What\'s your favorite Animal?',
		'answers': ['cat', 'dog', 'pig', 'owl'],
	},
];

var _questionIndex = 0;

child: Column(
	children: [
		Question(
			questions[_questionIndex]['questionText'] as String,
		),
		...(questions[_questionIndex]['answers'] as List<String>)
			.map((answer) {
				return Answer(answer);
		}).toList(),

],

),

```

```dart
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


return Column(
	children: [
		Question(
			questions[questionIndex]['questionText'] as String,
		),
		...(questions[questionIndex]['answers'] as List<Map<String, Object>>)
				.map((answer) {
			return Answer(
			() => answerQuestion(answer['score']), answer['text'] as String);
		}).toList(),
],
)
```

```dart
final List<Transaction> transactions = [
	Transaction(
		id: 't1',
		title: 'New Shoes',
		amount: 69.99,
		date: DateTime.now(),
	),
	Transaction(
		id: 't2',
		title: 'Weekly Groceries',
		amount: 16.53,
		date: DateTime.now(),
	),
];

Column(
	children: transactions.map((tx) { //children: [...] amismagivrad egreve vsvavt 
	                                  // radgan abrunebs List-s : .toList()
		return Card(
			child: Row(
				children: [
					Container(
						child: Text(
							'\$${tx.amount}',  //Stringshi gadayvanis ori metodi
						), // Text(tx.amount.toString()) toStringAsFixed(3)
					),
					Column(
						children: [
							Text(tx.title),
							Text(tx.date.toString()),
						],
					),
				],
			));
	}).toList(),
)
```