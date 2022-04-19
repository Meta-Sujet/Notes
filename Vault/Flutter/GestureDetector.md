If this widget has a child, it defers to that child for its sizing behavior. If it does not have a child, it grows to fit the parent instead.

When the user taps the [`Container`](https://api.flutter.dev/flutter/widgets/Container-class.html), the `GestureDetector` calls its [`onTap()`](https://api.flutter.dev/flutter/widgets/GestureDetector-class.html#onTap) callback, in this case printing a message to the console
```dart
void main() => runApp(
	MaterialApp(
		home: Scaffold(
			body: Center(
				child: MyButton(),
}

class MyButton extends StatelessWidget {
	Widget build(BuildContext context) {
		return GestureDetector(
			onTap: () {
				print('Button tapped');
			},
			child: Container(
				width: double.infinity,
				height: 50,
				padding: EdgeInsets.all(8),
				margin: EdgeInsets.symmetric(horizontal: 8),
				decoration: BoxDecoration(
					borderRadius: BorderRadius.circular(5),
					color: Colors.orange,
),
				child: Center(child: Text('Test'))),
);

}
```

```dart
class _MyStatefulWidgetState extends State<MyStatefulWidget> {

	bool _lightIsOn = false;
  
	Widget build(BuildContext context) {
		return Scaffold(
			body: Container(
				alignment: Alignment.center,
				child: Column(
					mainAxisSize: MainAxisSize.min,
					children: [
						Icon(
							Icons.lightbulb_outline,
							// Ternary in Propery/Argument !!! <----
							color: _lightIsOn ? Colors.yellow : Colors.black,
							size: 50,
						),
						GestureDetector(
							onTap: () {
								setState(() {
							_lightIsOn = !_lightIsOn;
							});
							},
							child: Container(
								color: Colors.orange,
								padding: EdgeInsets.all(10),
								width: 150,
								margin: EdgeInsets.only(top: 20),
									child: Text(
									// Ternary in Text !!! <-----
									_lightIsOn ? 'TURN LIGHT OFF':'TURN LIGHT ON',
									textAlign: TextAlign.center,


```

```dart
class _MyStatefulWidgetState extends State<MyStatefulWidget> {

Color _color = Colors.white;

Widget build(BuildContext context) {
	return Scaffold(
		body: Container(
			// constraints: BoxConstraints.expand(width: 200, height: 200),
			color: _color,
			child: GestureDetector(
				onTap: () {
					setState(() {
						_color == Colors.yellow
							? _color = Colors.white
							: _color = Colors.yellow;
				});

```