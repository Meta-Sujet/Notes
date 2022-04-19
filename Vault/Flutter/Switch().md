```dart
.... StatefulWidget {

bool _showChart = false;

Widget build(...) {
		....
		......
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