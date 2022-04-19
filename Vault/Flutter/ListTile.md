```dart
Card(
	elevation: 5,
	margin: EdgeInsets.symmetric(vertical: 8, horizontal: 5),
		child: ListTile(
			leading: CircleAvatar(
				backgroundColor: Theme.of(context).colorScheme.primary,
				radius: 30,
				child: Padding(
				padding: const EdgeInsets.all(10),
					child: FittedBox(
						child: Text(
							'\$${transactions[index].amount}',
							style: TextStyle(color: Colors.white),
							),
					),
				),
			),
			title: Text(
				transactions[index].title,
				style: Theme.of(context).appBarTheme.titleTextStyle,
			),
			subtitle: Text(
				DateFormat.yMMMd().format(transactions[index].date),
			),
			trailing: IconButton(
				icon: Icon(Icons.delete),
				color: Theme.of(context).errorColor,
				onPressed: () => deleteTx(transactions[index].id),
			),
),
)
```