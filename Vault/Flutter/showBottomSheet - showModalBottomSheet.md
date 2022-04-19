https://www.youtube.com/watch?v=TXYuaiukw7E

Modal BottomSheet:
```Dart
class MyApp extends StatelessWidget {
	static const String _title = 'Flutter';
	Widget build(BuildContext context) {
		return MaterialApp(
			title: _title,
			home: Scaffold(
				appBar: AppBar(title: Text(_title)),
				body: MyStatelessWidget(),


  
class MyStatelessWidget extends StatelessWidget {
	Widget build(BuildContext context) {
		return Center(
			child: ElevatedButton(
				child: Text('showBottomSheet'),
				onPressed: () {
					Scaffold.of(context).showBottomSheet((context) {
						return Container(
							height: 200,
							color: Colors.amber,
							child: Center(
								child: Column(
									children: [
										Text('BottomSheet'),
										ElevatedButton(
											onPressed: () {
												Navigator.pop(context);
												//Navigator.of(context).pop()
											},
											child: Text('Close BottomSheet'),

```

```dart
void _startAddNewTransaction(BuildContext ctx) {
	showModalBottomSheet(
		context: ctx,
		builder: (_) {
			return GestureDetector( // aq gesturedetectori ar sheidzleba 
                                    //cavushalot,arc hirdeba
				onTap: () => {},
				behavior: HitTestBehavior.opaque,
				child: NewTransaction(_addNewTransaction),
			);
		});
}

Widget build(BuildContext context) {
	return Scaffold(
		appBar: AppBar(
			title: Text('Flutter App'),
			actions: [
				IconButton(
					onPressed: () => _startAddNewTransaction(context),
					icon: Icon(Icons.add),
				),
			],
		),
		body: ... ,
		floatingActionButton: FloatingActionButton(
			child: Icon(Icons.add),
			onPressed: () => _startAddNewTransaction(context),
		)

--------------- an :

actions: [
	IconButton(
		onPressed: () => showModalBottomSheet(
			context: context,
			builder: (_) {
				return GestureDetector(
					onTap: () => {},
					behavior: HitTestBehavior.opaque,
					child: NewTransaction(_addNewTransaction),
				);
			}),
		icon: Icon(Icons.add),
	),
]


```

```dart
Navigator.of(context).pop(); ???
```