-stateless utility widget whose build method uses its builder callback to create the widget's child.
-this widget is a simple inline alternative to defining a StatelessWidget subclass.
-BuildContext can only get information of it's parents widgets and not of a child widget
-Most of the time ,widgets in flutter build without looking up any extra information about their parents but sometimes, you might write some code where child widget needs to access the build metodh.that's what the Builder widget is for. This scenario happens if you are accessing an inherited widget like: Scaffold,navigator,themedata,mediaquery or some methods of state management.

```Dart
class Foo extends StatelessWidget {
Widget build(BuildContext context) => Text('foo');
}

Center(child:Foo())

// Without defining new widget class:

Center(
	child: Builder(
		builder: (BuildContext context) => Tetxt('foo');
	)
)
```

-difference is extra BuildContext element that the additional widget adds.
-Scaffold.of method which visits the child widget's BuildContext ancestors.


```Dart
class MyApp extends StatelessWidget {

Widget build(BuildContext context) {

return MaterialApp(

home: MyHomePage(),

);

}

}


class MyHomePage extends StatelessWidget {

Widget build(BuildContext context) {

return Scaffold(

body: Center(

child: TextButton(

onPressed: () => {

//Fails because Scaffold.of doesn't find anything above this widget's context

//Scaffold.of() called with a context that does not contain a Scaffold.

//onPressed callback is unabel to find enclosing ScaffoldState with Scaffold.of

print(Scaffold.of(context).hasAppBar)

},

child: Text('hasAppBar'),

),

),

);

}

}
```

With builder: 
-Builder widget introduces on additional BuildContext element and so the Scaffold.of method succeeds

```Dart
class MyHomePage extends StatelessWidget {
	Widget build(BuildContext context) {
		return Scaffold(
			body: Builder(
				builder: (context) {
					return Center(
						child: TextButton(
						onPressed: () => {print(Scaffold.of(context).hasAppBar)},
						child: Text('hasAppBar'),

```


```Dart

class MyApp extends StatelessWidget {
	final String title = 'Builder';
	Widget build(BuildContext context) => MaterialApp(
		debugShowCheckedModeBanner: false,
		title: title,
		theme: ThemeData(primarySwatch: Colors.deepOrange),
		home: MainPage(title: title),
);
}

class MainPage extends StatefulWidget {

	final String title;

	MainPage({required this.title});

	_MainPageState createState() => _MainPageState();

}


class _MainPageState extends State<MainPage> {
	Widget build(BuildContext context) => Scaffold(
		appBar: AppBar(
		title: Text(widget.title),
),
		body: Builder(
			builder: (context) {
			return ElevatedButton(
				onPressed: () {
				Scaffold.of(context).showSnackBar(
				SnackBar(
				content: Text('hey'),
),
);
},
				child: Text('Show SnackBar'),
);
},
),

		floatingActionButton: FloatingActionButton(
			backgroundColor: Colors.blue,
			onPressed: () {},
			child: Icon(
				Icons.favorite,
				color: Theme.of(context).primaryColor,
),
),
);
}
```