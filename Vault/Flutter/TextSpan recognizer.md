```dart

// II - or use with variable:
final gestureRecognizer = TapGestureRecognizer()
..onTap = () => print('tapped'); <----cascade notation

-------- check this:
final gestureRecognizer = TapGestureRecognizer();
gestureRecognizer.onTap = () => print('tapped');
--------

// I
TextSpan(
	text: 'Register',
	style: TextStyle(
		color: Colors.blue,
	),
	recognizer: TapGestureRecognizer()
	..onTap = () => print('hey'),
	
	// II: recognizer: gestureRecognizer,
)

```