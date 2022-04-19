```dart
body: Center(
	child: RichText(
		text: TextSpan(
			text: 'Share',
			style: TextStyle(
				color: Colors.blue,
				fontSize: 50,
			),
			children: [
				WidgetSpan(
					child: Icon(
						Icons.share,
						color: Colors.red,
						size: 20,
					),
					alignment: PlaceholderAlignment.middle,

```

//
TextSpan(.....),
WidgetSpan(
		child: SizedBox(
			...
			...
			child: 
		)
),
TextSpan(.....)