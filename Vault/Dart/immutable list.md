```dart
//Finally, if you want an immutable list but you won’t know the element values until runtime, then you can create one with the List.unmodifiable named constructor:

final modifiableList = [DateTime.now(), DateTime.now()]; 
final unmodifiableList = List.unmodifiable(modifiableList);

unmodifiableList.add(DateTime.now());
print(unmodifiableList);   // Error

//DateTime.now() returns the date and time when it’s called. You’re obviously not going to know that until runtime, so this prevents the list from taking const. Passing that list into List.unmodifiable, however, makes the new list immutable.

final dateNow = 
	List.unmodifiable([DateTime.now().minute, DateTime.now().minute]);

dateNow.add(2); 

print(dateNow); //error

//Note: Unfortunately, inadvertently trying to modify an unmodifiable list will cause a runtime error — not a compile-time error. So while mutable data can be unsafe, so too can unmodifiable lists. A good practice is to write tests to ensure your code works as intended.
```