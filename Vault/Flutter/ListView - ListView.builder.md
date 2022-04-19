https://www.youtube.com/watch?v=KJpkjHGiI5A

https://www.youtube.com/watch?v=8vpC00KxeE4

https://www.youtube.com/watch?v=TdWhYERuv7g&t=180s

```dart

// automatically scrollable column or row: ListView.
// its kind of shortcut for SingleChildScrollView.
// ListView is column or row with SingleChildScrollView

Container(
	height: 300, // containeri aucileblad chirdeba tavisi heightit,torem ar gamochndeba. ListView-s heighti aris usasrulo,Columnis height ikavebs arsebuli heightis maqsimalurs. ase rom conteinerma unda sheuzgudos heighti.
	child: ListView(.  //changed Column with ListView
		scrollDirection: Axis.vertical,  // Axis.horizontal  = Row
		children: []

---------------
					
// ListView yvela ertad itvirteba imisdamiuxedavad chans tu ara ekranze.es aris gansxvaveba mat shoris
// ListView.builder only renders/loads widgets that are visible

body: Container(
	child: ListView.builder(
		itemCount: 20,
		itemBuilder: (context, index) {
			return ListTile(
				title: Text('List tile $index'),


// magram roca Parent widgeti aris Column an Row. ListView unda movaqciot Expanded() -shi. sxva shemtxvevashi ar gamochndeba sia..

body: Container(
	child: Column(
		children: [
			Expanded(
				child: ListView.builder(
					itemCount: 20,
					itemBuilder: (context, index) {
						return ListTile(
						title: Text('List tile $index'),
-------


return Container(
	height: 300,
	child: ListView.builder(
		itemCount: transactions.length,
		itemBuilder: (context, index) {
			return Card(...
			..........
				Text(transactions[index].title,

```