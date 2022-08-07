# DART BASICS

## Main function

```dart
    main(List<String> arguments) {
        print("Hello World");
    }
```

## Data Types

* Everything is object in Dart. Even primitive types are objects and have inbuilt methods
```dart
    print("".runtimeType);  // String
```
* Boolean (bool) :
```dart
    bool isNew = false;
    print("Hello World :  ${isNew ? 'Welcome back' : 'Welcome'}");
```
* We can use `var` to declare variable
```dart
    var text = "0";
    print(text.runtimeType);
```
* Numbers :
    * `num` : var for numbers
    ```dart
        num age = 0;
    ```
    * `int`
    ```dart
        int people = 6;
    ```
    * `double`
    ```dart
        double temp = 3.09;
    ```
    * Parsing integer
    ```dart
        int test = int.parse('12')  // Parsing string to int
        int test = int.parse('12.09')  // FormatException: Invalid radix-10 number
    ```
    * We can provide default values on error like below
    ```dart
        int test = int.parse('12.09', onError : (source) => 0)
        print('test : ${test}');    // 0
        // The code throws FormatException, So it runs the onError function and returns 0
    ```
    * `int`, `double`, etc are actually classes
    * `String`:
    ```dart
        String hello = 'Hello World';
        print(hello);
    ```
    * String operations
        ```dart
            String name = "Shinu Mathew";
            String firstName = name.substring(0, 5);
            // Instead of doing the above, we can get the start index by identifying the pattern and using a indexOf()
            int startIndex = name.indexOf(" ");
            // String lastName = name.substring(startIndex, name.length).trim();
            String lastName = name.substring(startIndex+1, name.length);
            print(firstName);
            print(lastName);

            // CONTAINS
            print(name.contains(lastName));

            // TO LIST
            List parts = name.split(' ');
            print(parts);
            print(parts[0]);
            print(parts[1]);
        ```
    * `const` variables
        ```dart
            const String name = "Shinu";
            name = "Ma";  // Constant variables can't be assigned a value.
        ```