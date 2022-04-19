- not shure how much space you have?
builds a widget tree that can depend on the parent widget's size.Provides the parent widget's constraints.

```dart
return LayoutBuilder(builder: (BuildContext context, BoxConstraints constraints){
	.... ... ...
	.... 
	constraints.maxWidth //minWidth, maxHeight, minHeight
})
```