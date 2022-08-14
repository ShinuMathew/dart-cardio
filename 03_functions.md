# FUNCTIONS IN DART

## Optional parameters
* We can declare a function with optional parameter. Ex : `([String name = ""])`
```dart
    main(List<String> arguments) {
        sayHello();
    }

    void sayHello([String name = ""]) {
        if(name.isNotEmpty) name = name.padLeft(name.length+1); // To avoid the space
    print('Hello${name}');
}
```
* Optional parameters should come as the last parameter

## Named Arguments
```dart
    main(List<String> arguments) {
        print(squareFeet(length : 10, width : 20));
    }

    int squareFeet({int width : 0, int length : 0}) {
        return width * length;
    }
```

## Functions as Objects
```dart
    main(List<String> arguments) {
        var squaring = squareFeet
        print(squaring(length : 10, width : 20));
    }

    int squareFeet({int width : 0, int length : 0}) {
        return width * length;
    }
```

## Anonymous functions
* ```dart
    var anon = () {
        print("anonymous");
    };

    anon();
  ```

## Function referrence
```dart
    List people = ['Bryan', 'Carla', 'Sujeeth'];
    
    people.forEach((element) {
        print(element);
    });

    print("============ CAN BE WRITTEN AS =============");

    people.forEach(print);
```