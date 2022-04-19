 Accessing elements from a map:
A map will return null if the key doesn’t exist. Because of this, accessing an element from a map always gives a nullable value. In the example above, Dart infers numberOfCakes to be of type int?. If you want to use numberOfCakes, then you need to treat it as you would any other nullable value.

```dart
final inventory = {
	'cakes': 20,
	'pies': 14,
	'donuts': 37,
	'cookies': 141,
};
  
final numberOfCakes = inventory['cakes']; <-- int?
print(numberOfCakes?.isEven);

int numberOfCakes = inventory['cakes'] as int;
print(numberOfCakes.isEven);

 
print(inventory.keys); 
print(inventory.values);
 

print(inventory.containsKey('pies')); 
print(inventory.containsValue(42));
```

```dart
//creating an empty map:
final Map<String, int> emptyMap = {};

shorter way: 

final emptyMap = <String, int>{};
```


Well, it turns out that map literals came before set literals in Dart’s history, so Dart infers the empty braces to be a Map of <dynamic, dynamic>; that is, the types of the key and value are both dynamic. If you want a set, and not a map, then you need to be explicit:

```dart
final mySet = <String>{};
```


Unlike lists, you can’t iterate over a map using a for-in loop. 
Iterable is a type that knows how to move sequentially, or iterate, over its elements. List and Set both implement Iterable, but Map does not. 

There is a solution, though, for looping over a Map. The keys and values properties of a map are iterables, so you can loop over them:
```dart
inventory.forEach((key, value) {
	print(key);
});


for (final entry in inventory.entries) {
	print('${entry.key} -> ${entry.value}');
}


for (var item in inventory.values) {
	print(item);
}


for (var item in inventory.keys) {
	print(item);
}


for (var item in inventory.keys) {
	print(inventory[item]);
}
```