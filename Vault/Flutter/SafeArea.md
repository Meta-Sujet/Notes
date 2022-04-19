```dart
EdgeInsets devicePadding = MediaQuery.of(context).viewPadding;

Size size = MediaQuery.of(context).size;

Orientation orientation = MediaQuery.of(context).orientation;
```

```Dart
Widget build(BuildContext context) {

Size size = MediaQuery.of(context).size;

Orientation orientation = MediaQuery.of(context).orientation;

double boxSide = size.shortestSide - 50;

return SafeArea(

top: true,

child: Scaffold(

body: Center(child: Text('hey')),

),

);

}
```
same with padding:
```Dart
Widget build(BuildContext context) {

EdgeInsets devicePadding = MediaQuery.of(context).viewPadding;


return Padding(

padding: devicePadding,

// padding: EdgeInsets.only(top: 25),

child: Scaffold(

body: Center(child: Text('hey')),

),

);

}
```