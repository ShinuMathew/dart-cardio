# PACKAGES IN DART

* Packages which are part of dart library can be simply imported as,
    ```dart
        import 'dart:io';
    ```
* Packages which are public needs to be added to `pubspec.yml` and then `pub get` to `install the dependencies`. Then it can be imported as,
    ```dart
        import 'package:path/path.dart' as myPath;
    ```
    * Dart takes the file `path.dart` in package `path` and converts it into a class in the memory and then we are calling that class as `myPath`