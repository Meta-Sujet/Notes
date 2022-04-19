```dart
bool? isBeautiful(String? item) {
	if (item == 'flower') {
		return true;
	} else if (item == 'garbage') {
		return false;
	}
	return null;
}

bool item = isBeautiful('flowser') ?? false;
print(item);

bool? item = isBeautiful('flowser');
print(item);

bool item = isBeautiful('flowser')!;
print(item);

bool item = isBeautiful('flowser') as bool;
print(item);

final item = isBeautiful('flowser'); //infers : bool?
print(item);

```

```dart
class TextWidget {
	String? text;
	bool isLong() {
		if (text == null) {
			return false;
		}
		return text.length > 100; // error
		return text!.length > 100; // so add ! <--now works
	}
}

------
 
//Another option is to shadow the non-local variable with a local one:

class TextWidget {
	String? text;
	bool isLong() {
		final text = this.text; //shadowing
		if (text == null) {
			return false;
		}
		return text.length > 100; 
	}
}
```