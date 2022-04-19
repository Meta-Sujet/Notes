```dart
import 'package:flutter/services.dart'

void main() {
	WidgetsFlutterBinding.ensureInitialized();
	
	SystemChrome.setPrefferedOrientations([
		DeviceOrientation.portraitUp,
		DeviceOrientation.portraitDown,
	])
}
```