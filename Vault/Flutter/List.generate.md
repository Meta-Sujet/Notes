```dart
List<Map<String, Object>> get groupedTransactionValues {
	return List.generate(7, (index) {
		final weekDay = DateTime.now().subtract(Duration(days: index));
		return {'day': DateFormat.E().format(weekDay), 'amount': 9.99};
});
}
```