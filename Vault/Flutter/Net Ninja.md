```dart
appBar: AppBar(
	title: Text('Flutter'),
	centerTitle: true,
	backgroundColor: Colors.grey[850],
	elevation: 0.0,
),
```

```dart
floatingActionButton: FloatingActionButton(
	child: Text('CLICK'),
	onPressed: () {},
)
```

```dart
body: Center(
	child: Image(
	// image: NetworkImage(''),
	image: AssetImage('assets/photo1.jpeg'),
),
),

-----------an widgetis chasmis gareshe:

body: Center(
	child: Image.asset('assets/photo1.jpeg'),
	child: Image.network('https: ......'),
),
```

```dart
var container = Container(
	width: double.infinity,
	height: double.infinity,
	color: Colors.yellow,
	child: Text('Hey'),
);
...
....
...
body: container,
```

```dart
//igive margin-is pontia, am shemtxvevashi marginivit mushaobs padingi

Padding(
	padding: const EdgeInsets.all(8.0),
	child: Container(
		color: Colors.red,
		child: Text('test'),
),
)
```

1.  Open the Command Palette ( Ctrl + Shift + P ( Cmd + Shift + P on macOS)).
2.  Select the Flutter: Inspect Widget command and press Enter.
3.  Tap on any widget in emulator.
4.  See the widget tree.
5.  Good luck.

// Rodesac shemogvaqvs surati Image() Row an Columnshi, defaultad aqvs tavisi zomebi , tu movaqcevt Expanded()-shi sheamcrirebs zomas ... 

```dart
CircleAvatar(
	backgroundImage: AssetImage('assets/partyhard.png'),
	radius: 50,
	// child:
)
```

```dart
Divider(
	color: Colors.amberAccent[200],
	height: 60,
	// thickness: 1,
	// indent: 100,
	// endIndent: 100,
),
```

```dart
Scaffold(
	backgroundColor: Colors.grey[900],
	appBar:....,
	body: ....,
```

```dart

ASYNCHRONOUS CODE

// main.dart
return MaterialApp(
	debugShowCheckedModeBanner: false,
	initialRoute: '/home',
	routes: {
		'/': (context) => Loading(),
		'/home': (context) => Home(),
		'/location': (context) => ChooseLocation(),
},


// home.dart
TextButton.icon(
	onPressed: () {
		Navigator.pushNamed(context, '/location');
	},
	icon: Icon(Icons.edit_location),
	label: Text('Edit Location'),
)

// choose_location.dart
int counter = 0;

void getData() async {
	String name = await Future.delayed(Duration(seconds: 3), () {
		return 'Korben';
	});

	print(name);
}

//void getData() {
//	Future.delayed(Duration(seconds: 3), () {
//		return 'Korben';
//	});
//}


void initState() {
	super.initState();
	getData();
	print('initState function run');
}

@override
Widget build(BuildContext context) {
	print('build function ran');
	return Scaffold(
		appBar: AppBar(
			title: Text('Choose Location'),
			centerTitle: true,
			elevation: 0,
		),
		body: ElevatedButton(
			child: Text('Counter: $counter'),
				onPressed: () {
					setState(() {
						counter++;
					});
				},
		),
	);

}
```