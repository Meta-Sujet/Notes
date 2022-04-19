https://www.kindacode.com/article/customize-borders-of-textfield-textformfield-in-flutter/
https://www.youtube.com/watch?v=C5hJIKCTrvk

input values are always String (if we need number we should convert it manually)

```dart

//rodesac vqmnit cvlads StatelessWidget-shi fluteri gveubneba rom gavxadot es cvladebi final .(final gavucerot) magram tu am shemtxvevashi gavucert finals ar gvacyobs.
//arsebobs meore gza user inputis dasacheratd. 
String? titleInput;  //outside build method
String? amountInput;

TextField(
	decoration: InputDecoration(labelText: 'Title'),
	onChanged: (String val) => titleInput = val,      //fetch user input
),
TextField(
	decoration: InputDecoration(labelText: 'Amount'),
	onChanged: (String val) => amountInput = val,
	keyboardType: TextInputType.number,
	//on iOS use this below: 
	//keyboardType: TextInputType.numberWithOptions(decimal: true),
)

// fetch user input, second way: 


//flutter has built-in mechanism that allows you to listen every key stroke and get finished value when done: 
//am shemtxvevashi finalis problemac mogvarebulia,shegvidzlia gavucerot cvlads final.

// TextEditingController() aris flutteris "shemotavazebuli" klasi,romelsac vanichebt/vabavt TextField()-s controller argumentis daxmarebit.
//flutter avtomaturad akavshirebs controller-s TextField-tan. controlleri usmens user inputs and save it.

final titleController = TextEditingController();   //outside build method
final amountController = TextEditingController();

TextField(
	decoration: InputDecoration(labelText: 'Title'),
	controller: titleController,      //fetch user input
),
TextField(
	decoration: InputDecoration(labelText: 'Amount'),
	controller: amountController,      //fetch user input
),
TextButton(
	onPressed: () {
		print(titleController.text);  //titleControler.text 
		print(amountController.text);
	},
	child: Text('Add Transaction'),
	style: TextButton.styleFrom(primary: Colors.purple),
)

```

```dart
void submitData() {
	addNewTransaction(
		titleController.text,
		double.parse(amountController.text),
	);
}

TextField(
	decoration: InputDecoration(labelText: 'Amount'),
	keyboardType: TextInputType.number,
	onSubmitted: (_) => submitData(), //anonymous function
	// _ means : I get an argument but i dont care about it.
),
TextButton(
	onPressed: submitData,
	child: Text('Add Transaction'), // dacherisas gaitishos keyboardi
	style: TextButton.styleFrom(primary: Colors.purple),
)
```

```dart
final titleController = TextEditingController();
final amountController = TextEditingController();

void submitData() {
	final enteredTitle = titleController.text;
	final enteredAmount = double.parse(amountController.text);
  
	if (enteredTitle.isEmpty || enteredAmount <= 0) {
		return; //code after return is not reached.return stops function execution
	}
 
	addNewTransaction(
		titleController.text,
		double.parse(amountController.text),
	);
}
```