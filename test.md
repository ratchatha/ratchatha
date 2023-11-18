```
mkdir node-express
```


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


```Dart
void sayHello() { // A top-level function
  print("Hello, world!");
}
void main() {
  sayHello(); // "Hello, world!"
}

```
