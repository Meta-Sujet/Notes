box/widget with a specific size that directs its child to also have that size.

we can use SizedBox without child,it will not render anything,
but will still take out place. Gaps between widgets !!!

```dart
body: Container(
	width: 200, // SizedBox-s width and height will be 200 not 100.
	height: 200,
	child: SizedBox(
		width: 100, //double.infinity // if in container dont have width height,can use this sizes
		height: 100,
		child: ElevatedButton(
			child: Text('button'),
				onPressed: () {},
```

```dart
SizedBox.expand() // full width&height of parent widget
```

```dart
Column(
	children: [
	MyButton(),
	SizedBox(height: 100),
	MyButton(),
	]
```

```dart
body: SizedBox(
	width: 200,  // am shemtxvevashi zomebi iqneba 200 da ara 150
	height: 200,
	child: Container(
		width: 150, //ignored
		height: 150,
		color: Colors.red,
```

```Dart
SizedBox.square(
	dimension:500,     /creates box whose width and height are equal
)
```