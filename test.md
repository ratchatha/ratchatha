
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
![image](https://github.com/ratchatha/ratchatha/assets/141728801/887041b7-4214-4951-bc0a-c3b63b016584)
```
