```DART
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
	Widget build(BuildContext context) {
		return MaterialApp(
			home: MyHomePage(),
);
}
}

  

class MyHomePage extends StatelessWidget {
Widget build(BuildContext context) {

Size size = MediaQuery.of(context).size;

return Scaffold(
	body: Center(
		child: Container(
			color: Colors.red,
			width: size.shortestSide,
			height: size.shortestSide,
			
			width: size.width / 2,
			height: size.width / 2,
),
),
);
}
}
```

```Dart
class MyApp extends StatelessWidget {
	Widget build(BuildContext context) {
		return MaterialApp(
			home: MyHomePage(),
		);
	}
}

class MyHomePage extends StatelessWidget {
	List<Widget> layoutChildren(double boxSide) {
		return [
			Container(
				width: boxSide,
				height: boxSide,
				color: Colors.green,
				alignment: Alignment.center,
				child:
				Text('one', style: TextStyle(fontSize: 30, color: Colors.blue))),
			Container(
				width: boxSide,
				height: boxSide,
				color: Colors.red,
				alignment: Alignment.center,
				child: Text('one',
				style: TextStyle(fontSize: 30, color: Colors.orange))),
];
}
  
Widget build(BuildContext context) {
	Size size = MediaQuery.of(context).size;
	Orientation orientation = MediaQuery.of(context).orientation;
	double boxSide = size.shortestSide - 50;
	return SafeArea(
		top: true,
		child: Scaffold(
			body: Center(
				child: Container(
					width: size.width / 2,
					height: size.width / 2,
					color: Colors.blue,
					child: Text('${orientation.index}'),
),
),
),
);
}
}
```

With Builder :  

```dart
Widget build(BuildContext context) {
	Size size = MediaQuery.of(context).size;
	Orientation orientation = MediaQuery.of(context).orientation;
	double boxSide = size.shortestSide - 50;
		return SafeArea(
		top: true,
		child: Scaffold(
			body: Center(
				child: Builder(
					builder: (context) {
						return Container(
							width: size.width / 2,
							height: size.width / 2,
							color: Colors.blue,

```

```dart
Widget build(BuildContext context) {
Size size = MediaQuery.of(context).size;
Orientation orientation = MediaQuery.of(context).orientation;
double boxSide = size.shortestSide - 50;

return Center(
	child: Builder(
		builder: (context) {
			if (orientation.index == Orientation.landscape.index) {
				return Center(
					child: Row(
						mainAxisAlignment: MainAxisAlignment.center,
						children: layoutChildren(boxSide),
),
);
			} else {
				return Column(
					children: layoutChildren(boxSide),
);
}
```