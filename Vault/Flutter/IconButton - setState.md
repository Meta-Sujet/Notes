```Dart
class MyApp extends StatelessWidget {
	static const String _title = 'Flutter';
	Widget build(BuildContext context) {
		return MaterialApp(
			title: _title,
			home: Scaffold(
				appBar: AppBar(title: Text(_title)),
				body: Center(
					child: MyStatefulWidget(),
}


class MyStatefulWidget extends StatefulWidget {
State<MyStatefulWidget> createState() => _MyStatefulWidget();
}


class _MyStatefulWidget extends State<MyStatefulWidget> {

	double _volume = 0.0;

	Widget build(BuildContext context) {
		return Column(
			mainAxisAlignment: MainAxisAlignment.center,
			children: [
				IconButton(
					icon: Icon(Icons.volume_up),
					tooltip: 'Increase volume',
					onPressed: () {
						setState(() {
							_volume += 10;
						});
},
),
				Text('Volume: ${_volume.toStringAsFixed(0)}'),
],
);

}

}
```