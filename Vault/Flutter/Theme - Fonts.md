```dart
return MaterialApp(
	debugShowCheckedModeBanner: false,
	theme: ThemeData(
		primarySwatch: Colors.purple,
		accentColor: Colors.orange,  // deprecated
		// colorScheme: ColorScheme.light(),
	),
	title: 'Personal Expenses',
	home: MyHomePage(),
);

style: TextStyle(
	fontSize: 20,
	color: Theme.of(context).primaryColor,
),

border: Border.all(
	color: Theme.of(context).primaryColor,
	width: 2,
),

```

```Dart
theme: ThemeData(
	//primarySwatch: Colors.purple,
	//accentColor: Colors.orange, 
	colorScheme: ColorScheme.light().copyWith(
		primary: Colors.purple,
		secondary: Colors.orange,
	),
	fontFamily: 'Quicksand',
	textTheme: TextTheme(
		headline6: TextStyle(
			color: Colors.red,
			backgroundColor: Colors.yellow,
			),
		),
		button: TextStyle(
			color: Colors.white,
		),
	appBarTheme: AppBarTheme(          //yvela appbaris title textis style
		titleTextStyle: TextStyle(
			fontFamily: 'OpenSans',
			fontSize: 18,
			fontWeight: FontWeight.bold,
		),
	),
)


style: TextStyle(
	fontSize: 20,
	color: Theme.of(context).colorScheme.primary,
),

border: Border.all(
	color: Theme.of(context).colorScheme.primary,
	width: 2,
),


// magalitad shegvidzlia appbar titles style mivanichot nebismier sxvagan arsebul teqsts
Text(
	'Test',
	style: Theme.of(context).appBarTheme.titleTextStyle,
)


// an calke gavcerot chveni Theme teqstistvis
Text(
	'Test',
	// style: Theme.of(context).appBarTheme.titleTextStyle,
	style: Theme.of(context).textTheme.headline6,
)

--------pubspec.yaml: (in fonts section)
fonts:
	- family: OpenSans
	  fonts:
		- asset: assets/fonts/OpenSans-Regular.ttf
		- asset: assets/fonts/OpenSans-Bold.ttf
			weight: 700
	- family: Quicksand
	  fonts:
		- asset: assets/fonts/Quicksand-Regular.ttf
		- asset: assets/fonts/Quicksand-Bold.ttf
			weight: 700

```