# ERROR HANDLING

`Dart has 2 concepts. An Error and an Exemption`

* Error : Its a program failure
* Exemption : Can be handled

```dart
    try {
 
    } catch(e) {

    } finally {

    }
```

* We can catch specific error
```dart
    try {
 
    }
    on NoSuchMethodError {
        print("Sorry")
    } catch(e) {

    } finally {

    }
```

* We can throw exception using 
```dart
    if(age == null) throw new NullThrownError();
```
