```dart
body: Container(
	child: _questionIndex < questions.length
		? Column(
			children: [
				Question(
				questions[_questionIndex]['questionText'] as String,
				),
				...(questions[_questionIndex]['answers'] as List<String>)
				.map((answer) {
				return Answer(_answerQuestion, answer);
				}).toList(),
			],
		)
		: Container(
			child: Center(
			child: Text('Finished!'),
		),
			
),

),
```