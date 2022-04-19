A widget that positions its children relative to the edges of its box.

This class is useful if you want to overlap several children in a simple way, for example having some text and an image, overlaid with a gradient and a button attached to the bottom.

```dart
body: Container(
	color: Colors.yellow,
	padding: EdgeInsets.all(20),
	constraints: BoxConstraints.expand(width: 300, height: 300),
	child: Stack(
		fit: StackFit.loose, //containers cant be more height or width than 
							// containers width height, if we write it
							
	-->	fit: StackFit.expand, //non-positioned children will beexpanded to take 
                              //maximum height&width
		clipBehavior: Clip.none,
		alignment: Alignment.bottomLeft,
		children: [
			Container(width: 200, height: 200, color: Colors.red),
			Container(width: 150, height: 150, color: Colors.blue),
			Positioned(
				width: 120, //overrides container size. 100 x 100 will be overriden
				height: 110, //overrides too
				bottom: -50,
				child:
				Container(width: 100, height: 100, color: Colors.green)),

```

```Dart
body: Center(
	child: Container(
		width: 200,
		height: 200,
		color: Colors.blue,
		child: Stack(
			clipBehavior: Clip.none,
			children: [
				Positioned(
					height: 250,
					child: Container(
						color: Colors.red,
						width: 100,
						height: 250,

```