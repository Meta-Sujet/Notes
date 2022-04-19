```dart
ElevatedButton(
	style: ButtonStyle(
		backgroundColor: MaterialStateProperty.all(Colors.red),
		foregroundColor: MaterialStateProperty.all(Colors.black),
		textStyle: MaterialStateProperty.all(TextStyle(fontSize: 20))),
	onPressed: selectHandler,
	child: Text(answerText),
),

------

ElevatedButton(
	style: ElevatedButton.styleFrom(
		primary: Colors.green,  //background color
		onPrimary: Colors.black,
		elevation: 10,
		alignment: Alignment.topCenter,
		textStyle: TextStyle(fontWeight: FontWeight.bold)),
	onPressed: selectHandler,
	child: Text(answerText),
)

-----

ElevatedButton(
	style: ElevatedButton.styleFrom(
		minimumSize: Size(200, 20),  // width height
		// an 
		minimumSize: Size.fromHeight(20), // automatically expands full width
	),
	onPressed: selectHandler,
	child: Text(answerText),
)
```

```dart
TextButton(
	style: TextButton.styleFrom(
		primary: Colors.green,  // Text color
		textStyle: TextStyle(fontSize: 22)),
	onPressed: selectHandler,
	child: Text(answerText),
)
```

```dart
OutlinedButton(
	style: OutlinedButton.styleFrom(
		shape: StadiumBorder(),
		side: BorderSide(width: 2, color: Colors.green),
		backgroundColor: Colors.orange,
		textStyle: TextStyle(fontSize: 20)),
	onPressed: selectHandler,
	child: Text(answerText),
)
```

```dart
IconButton(
	onPressed: selectHandler,
	icon: Icon(
		Icons.settings,
		color: Colors.blueAccent,
	),
	iconSize: 50,
)

-------

ElevatedButton.icon(   //TextButton.icon(). OutlinedButton.icon()
	onPressed: selectHandler,
	icon: Icon(
		Icons.settings,
	),
	label: Text('Elevated Button'),
	
	// an adgili shevucvalot icons da teqsts
	
	label: Icon(
		Icons.settings,
	),
	icon: Text('Elevated Button'),
)
```