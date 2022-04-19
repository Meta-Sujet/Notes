Scales and positions its child within itself according to [fit](https://api.flutter.dev/flutter/widgets/FittedBox/fit.html).

```dart
Container(
	height: 300,
	width: 100,
	color: Colors.red,
	child: FittedBox(
		alignment: Alignment.center,
		clipBehavior: Clip.hardEdge,
		fit: BoxFit.cover,
		child: Image.network(
		'https://flutter.github.io/assets-for-api-docs/assets/widgets/owl-2.jpg'),
		),
)
```

```dart
Container(
	height: 200,
	width: 300,
	color: Colors.green,
	child: FittedBox(
		child: Text(
			'Flutter',
			style: TextStyle(
				color: Colors.white,
				fontSize: 300, // orive shemtxvevashi agar aqcevs yuradgebas fontis zomas da zrdis maqsimalurad tavis zomebdshi
				fontSize: 30 //
-----------

Container(
	height: 200,
	width: 300,
	color: Colors.green,
	child: FittedBox(
		fit: BoxFit.scaleDown, <---------
		child: Text(
			'Flutter',
			style: TextStyle(
				color: Colors.white,
				fontSize: 30 // dapataraveba romc mogvindes ver movaxerxebt am shemtxvevahsi unda gmaoviyenot : fit

```