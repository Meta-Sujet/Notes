A widget that controls how a child of a [Row](https://api.flutter.dev/flutter/widgets/Row-class.html), [Column](https://api.flutter.dev/flutter/widgets/Column-class.html), or [Flex](https://api.flutter.dev/flutter/widgets/Flex-class.html) flexes.

Using a [Flexible](https://api.flutter.dev/flutter/widgets/Flexible-class.html) widget gives a child of a [Row](https://api.flutter.dev/flutter/widgets/Row-class.html), [Column](https://api.flutter.dev/flutter/widgets/Column-class.html), or [Flex](https://api.flutter.dev/flutter/widgets/Flex-class.html) the flexibility to expand to fill the available space in the main axis (e.g., horizontally for a [Row](https://api.flutter.dev/flutter/widgets/Row-class.html) or vertically for a [Column](https://api.flutter.dev/flutter/widgets/Column-class.html)), but, unlike [Expanded](https://api.flutter.dev/flutter/widgets/Expanded-class.html), [Flexible](https://api.flutter.dev/flutter/widgets/Flexible-class.html) does not require the child to fill the available space.

A [Flexible](https://api.flutter.dev/flutter/widgets/Flexible-class.html) widget must be a descendant of a [Row](https://api.flutter.dev/flutter/widgets/Row-class.html), [Column](https://api.flutter.dev/flutter/widgets/Column-class.html), or [Flex](https://api.flutter.dev/flutter/widgets/Flex-class.html),

```dart
Flexible(
	flex: 2,
	fit: FlexFit.tight,  // daikavos mtliani shesadzlo adgili,
	child: Container(
		height: 100,
		child: Text('Item 2'),
		color: Colors.blue,
),
),
Flexible(
	flex: 1,
	fit: FlexFit.loose,  // daikavos imdeni adgili ramdenic chirdeba teqsts(am shemtxvevahsi)
	child: Container(
		height: 100,
		child: Text('Item 3'),
		color: Colors.orange,
),
)
```


Expanded() - is simply Flexible() with fit: FlexFit.tight. and therefore Expanded  has no fit: argument .it only has flex: configuration.

```dart
Expanded(
	flex: 2,
	child: Container(
		height: 100,
		child: Text('Item 2'),
		color: Colors.blue,
),
),
Expanded(
	flex: 1,
	child: Container(
		height: 100,
		child: Text('Item 3'),
		color: Colors.orange,
),
)
```