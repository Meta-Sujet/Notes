--------pubspec.yaml: (in assets images section): 
```dart
assets:
	- assets/images/waiting.png
```

```dart
Container(
	height: 200,
	child: Image.asset(
		'assets/images/waiting.png',
		fit: BoxFit.cover,
	),
)
```