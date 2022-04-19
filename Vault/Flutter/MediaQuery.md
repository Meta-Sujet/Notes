- class / object - we have to connect it to our context with .of context because context is metadata object with some info about our widget and its position in the tree.
```dart
MediaQuery.of(context).size.width /height/longestSide/shortestSide
					  .orientation.index /name
					  .padding.top /bottom ...
					  .viewPadding.bottom /top ...
					  .viewInsets.top /bottom ...

MediaQuery.of(context).size.height * 0.6
// 60% of the available height of the screen
```

- access viewInsets property that gives us info about anything that's overlapping into our view, ex: Keyboard , and then we get a bottom property which tells us how much space is occupied by that keyboard
```dart
SingleChildScrollView(
	child: Card(
		child: Container(
			padding: EdgeInsets.only(top: 10, left: 10, right: 10,
			bottom: MediaQuery.of(context).viewInsets.bottom + 10
			)
		)
	)
)

showModalBottomSheet(
	isScrollControlled: true,
	context: context,
	builder: (_) {return newTransaction}
)
```

```dart
Orientation.portrait /landscape <- 0 portrait, 1 landscape index

final mediaQuery = MediaQuery.of(context);



final appBar = AppBar(title: ........);
// appbar object can now access anywhere since it stored in variable has info about height of the appbar.
Container(
	height: (MediaQuery.of(context).size.height -
			appBar.preferredSize.height - 
			MediaQuery.of(context).padding.top) * 0.5, <--statusbar padding
)


final scaleFactor = MediaQuery.of(context).textScaleFactor; <-- by default is 1
Text('txt', style: TextStyle(fontSize: 20 * scaleFactor))


final isLandscape = MediaQueri.of(context).orientation == Orientation.landscape;
....
......
childre: [
	if(isLandscape)
		Row(....),
	if(!isLandscape)
		Container(...),
	if(!isLandscape)
		txListWidget,
	if(isLandscape)
		_showChart ? Container() : txListWidget
]

final txListWidget = Container(....);

```