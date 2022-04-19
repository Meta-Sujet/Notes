```dart
.... StatefulWidget {

bool _showChart = false;

Widget build(...) {
		....
		......
		// Switch.adaptive() <-- automaticall adjust the look based on platform(Android/iOS)
		Switch( 
			value: _showChart,
			onChange: (vale) {
				setState(() {
					_showChart = val
				})
			}
		)
}
}
```