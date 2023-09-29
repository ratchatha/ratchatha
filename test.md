
```Dart
class Box<T> {			
  T value;
  Box(this.value);
}

void main() {
  var integerBox = Box<int>(42);
  var stringBox = Box<String>("Hello, Dart!");

  print(integerBox.value); // 42
  print(stringBox.value); // "Hello, Dart!"
}
```
