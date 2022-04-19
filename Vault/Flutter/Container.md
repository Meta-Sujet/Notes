```dart
padding: EdgeInsets.lerp(EdgeInsets.all(10), EdgeInsets.all(20), 1),

// tu boloshi gavucert 0-s pading iqneba 10,
// tu 1-s pading iqneba 20
```

```dart
//igivea rac width: double.infinity, height: double.infinity,
//all available width&height
constraints: BoxConstraints.expand(),

constraints: BoxConstraints.expand(width: 200, height 200),



constraints: BoxConstraints(
	minWidth: 200,
	maxWidth: double.infinity,
	minHeight: 200,
	maxHeight: double.infinity,
)
```

```dart
// tu containers ar aqvs gacerili zomebi,mashin alignment-i avtomaturad gazrdis konteineris zomas maqsimalurad, width&height. da childs moaqcevs centrshi
// igivea rom conteiners qondes gacerili BoxConstraints.expand()
// tu width & height mititebuli gvaqvs, am zomis farglebshi moatavsebs
alignment: Alignment.center, 
```

```dart
decoration: BoxDecoration(
	border: Border.all(
		color: Colors.red,
		width: 2,
		style: BorderStyle.solid,
	),
	borderRadius: BorderRadius.all(
		Radius.circular(20),
	),
	// an 
	borderRadius: BorderRadius.only(topLeft: Radius.circular(20))
	// an
	borderRadius: BorderRadius.circular(5)
)
------or------
// amastan border radiusi ar mushaobs
decoration: BoxDecoration(
	border: Border(
		bottom: BorderSide(
			color: Colors.green,
			width: 5,
)),
)


```

```dart
boxShadow: [
	BoxShadow(
		color: Colors.orange,
		blurRadius: 5,
		spreadRadius: 5,
		offset: Offset(10, 10),
	),
]
```

```dart
gradient: LinearGradient(
	colors: [
		Colors.black.withAlpha(0),
		Colors.black45,
	],
	begin: Alignment.topCenter,
	end: Alignment.bottomCenter,
),
```

```dart
body: Container(
	margin: EdgeInsets.all(20),
	width: 200,
	height: 200,
	clipBehavior: Clip.antiAlias, // <-----
	decoration: BoxDecoration(
		color: Colors.red,
		shape: BoxShape.circle,  // <----
	),
	child: Text(
		'Container Text',
		style: TextStyle(fontSize: 30),
)
```

```dart

transform: Matrix4.rotationZ(0.5),

```
