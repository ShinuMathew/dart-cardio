# Collections

## Enums

* `enum` should be declared outside the main function
    ```dart
    enum Colors {red, blue, green}

    main(List<String> arguments) {
          // Enum
        print(Colors);  //Colors
        print(Colors.values); //[Colors.red, Colors.blue, Colors.green]
        print(Colors.red);  //Colors.red
    }
    ```

## Lists

* Dart does not have a concept of an array
* They have collections and the king of the collection is `List`
* List has a '0' based index
```dart
    List test = [1, 2, 3 ,4];
    print(test.length);
    print(test[0]);
```
* We can have a functional List which can hold any type
```dart
    List things = new List();
    things.add(1);
    things.add('cats');
    things.add(true);
```
* This wont work in null safety. We need to use `generate` or `filled`
```dart
    var things = List.filled(3, 0); //[0, 0, 0]
    things[0] = 2;
    print(things);  //[2, 0, 0]
```
```dart
    var things = List.filled(3, 0); // Initial size and default value should be given
    things[0] = 2;
    print(things);

    var things2 = List.generate(3, (i) => i); // We use generate if an initial size needs to be provided but each element needs to be computed
    print(things2);
```

## Set

* Sets are unordered and does not allow duplicate
```dart
    Set things = new Set();
    things.add(1);
    things.add("cat");
    things.add(0.99999);
    things.add(true);
    things.add("cat");  // Duplicate not allowed so not entered
    print(things);  // {1, cat, 0.99999, true}
```

## Queue

* Ordered, no index and adds or removes from the start and end.
```dart
    Queue<int> things = new Queue();
    things.add(1);
    things.add(2);
    things.add(3);
    things.add(4);
    things.removeFirst();
    things.removeLast();
    things.addLast(6);
    things.addFirst(7);
    print(things);  // {7, 2, 3, 6}
```

## Maps

* Key value pair
```dart
    Map<String, int> peoples = {'Engineers': 3, 'Doctors': 4, 'Architects' : 5};
    peoples.putIfAbsent('CA', () => 30);
    print(peoples);
    print(peoples.keys);    // (Engineers, Doctors, Architects, CA)
    print(peoples.values);  // (3, 4, 5, 30)
    print('No of Engineers : ${peoples['Engineers']}');
```