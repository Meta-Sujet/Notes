```dart
import 'package:flutter/services.dart';

void main() {
	WidgetsFlutterBinding.ensureInitialized();
	SystemChrome.setPreferredOrientations([
		DeviceOrientation.portraitDown,
		DeviceOrientation.portraitUp,
	]);
	runApp(MyApp());
}
```