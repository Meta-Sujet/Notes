```dart
//Sets are used to create a collection of unique elements
//Duplicates are not allowed in a set, in contrast to lists, which do allow duplicates.
//You can also think of sets as a bag of elements with no particular ordering, unlike lists, which do maintain a specific order. Because order doesn’t matter in a set, sets can be faster than lists, especially when dealing with large datasets.
```

```dart
final setA = {1, 2, 3, 4, 5};
final setB = {3, 4, 5, 6, 7};

List test = [...setA];

List test = setA.toList(); <-- am shemtvevashi iterable-s abrunebs da gvicevs 
                                convertacia listshi
print(test);

final intersection = setA.intersection(setB); //3 4 5 
final union = setA.union(setB); // 1 2 3 4 5 6 7 
```

 

Almost everything that you learned earlier about lists also applies to sets. Specifically, you can perform any of the following operations with sets:

-   collectionif
    
-   collectionfor
    
-   for-in loops
    
-   forEach loops
    
-   spread operators