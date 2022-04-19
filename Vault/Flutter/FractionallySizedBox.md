A widget that sizes its child to a fraction of the total available space

```dart
SizedBox.expand(
      child: FractionallySizedBox(
        widthFactor: 0.5, // 50% of available size
        heightFactor: 0.5,
        alignment: FractionalOffset.centerRight,
        child: DecoratedBox(
          decoration: BoxDecoration(
            border: Border.all(
              color: Colors.blue,
              width: 4,
```

use it with no child for fractionally sized whitespace, :

-with flexible widget in row or column:

```dart
Flexible(
 child: FractionallySizedBox(
	 heightFactor: 0.1,
 )
)
```