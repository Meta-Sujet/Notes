`StatefulWidgets` are special widgets that know how to generate `State` objects, which are then used to hold state.

`StatefulWidget` and `State` are separate objects. In Flutter, these two types of objects have different life cycles. `Widgets` are temporary objects, used to construct a presentation of the application in its current state. `State` objects, on the other hand, are persistent between calls to `build()`, allowing them to remember information.

```dart
void main() {
	runApp(
		const MaterialApp(
			home: Scaffold(
			body: Center(
				child: Counter(),
}
  

class Counter extends StatefulWidget {
	const Counter({Key? key}) : super(key: key);
	
	@override
	_CounterState createState() => _CounterState();
}


class _CounterState extends State<Counter> {
	int _counter = 0;

	// an es:
	void _increment() {
		setState(() {
			_counter++;
		});
	}

	@override
	Widget build(BuildContext context) {
		return Row(
			mainAxisAlignment: MainAxisAlignment.center,
			children: <Widget>[
				ElevatedButton(
					onPressed: _increment, << //da es  
					onPressed: () {
						setState(() {
						_counter++;
						});
					},
					child: Text('Increment'),
					),
				SizedBox(width: 16),
				Text('Count: $_counter'),
],

```

the separation of responsibility allows greater complexity to be encapsulated in the individual widgets, while maintaining simplicity in the parent:

```Dart
void main() {

runApp(

const MaterialApp(

home: Scaffold(

body: Center(

child: Counter(),

),

),

),

);

}

  

class CounterDisplay extends StatelessWidget {

const CounterDisplay({required this.count, Key? key}) : super(key: key);

  

final int count;

  

@override

Widget build(BuildContext context) {

return Text('Count: $count');

}

}

  

class CounterIncrementor extends StatelessWidget {

const CounterIncrementor({required this.onPressed, Key? key})

: super(key: key);

  

final VoidCallback onPressed;

  

@override

Widget build(BuildContext context) {

return ElevatedButton(

onPressed: onPressed,

child: const Text('Increment'),

);

}

}

  

class Counter extends StatefulWidget {

const Counter({Key? key}) : super(key: key);

  

@override

_CounterState createState() => _CounterState();

}

  

class _CounterState extends State<Counter> {

int _counter = 0;

  

void _increment() {

setState(() {

++_counter;

});

}

  

@override

Widget build(BuildContext context) {

return Row(

mainAxisAlignment: MainAxisAlignment.center,

children: <Widget>[

CounterIncrementor(onPressed: _increment),

const SizedBox(width: 36),

CounterDisplay(count: _counter),

],

);

}

}
```


