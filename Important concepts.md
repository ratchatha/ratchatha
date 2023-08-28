# Important concepts
ใน tutorial นี้เราจะมาดูเรื่องแนวคิดที่สำคัญของ Dart  โดยที่ภาษา Dart เป็นภาษาโปรแกรมที่มีแนวคิดแบบ Object-Oriented Programming (OOP) ที่ให้ความสำคัญกับการจัดการกับ Object และ Class และใช้ในสร้าง Applications หรือ Project อื่นๆ และจะต้องคำนึงถึงข้อเท็จจริงและแนวคิดดังนี้
## Objects & Class
ใน Dart นั้นทุกอย่างคือวัตถุ และวัตถุทั้งหมดเป็น instance ของ class ซึ่งรวมถึงตัวเลข ฟังก์ชัน และค่าว่างถือเป็นวัตถุ อ็อบเจ็กต์ทั้งหมดจะสืบทอดมาจากคลาส Object ยกเว้นค่า null ถ้าหากใช้ sound null safety

## Null Safety
Dart เวอร์ชัน 2.12 ขึ้นไปที่เปิดใช้งาน null safety เมื่อประกาศตัวแปรจะต้องระบุว่าตัวแปรนั้นจะมีค่า null ซึ่งหมายความว่าตัวแปรไม่สามารถมีค่าว่างได้ 

### Example  
```dart
  void main() {
    String name;  
    print(name);  
  }
```
- Output
  
``` dart
Error: Non-nullable variable 'name' must be assigned before it can be used.
```

จากตัวอย่างจะทำให้เกิดการ runtime error หากต้องการระบุว่าตัวแปรอาจมีค่าเป็น null จะต้องเพื่มเครื่องหมายคำถาม ? ไปที่ประเภทข้อมูล 

### Example 
```dart
  void main() {
    String? name;  // ประกาศตัวแปร name โดยระบุว่าอาจจะมีค่าเป็น null
    print(name);  
  }
```
- Output
  
``` dart
null
```
## Type Annotations & Type Inference

### Type Annotations
คือภาษาที่ต้องมีการประกาศ และบอกว่าตัวแปรนี้จะเป็นข้อมูลประเภทไหนซึ่งตัวเราเองจะต้องกำหนดว่าตัวแปร ฟังก์ชัน วัตถุ นั้นมี type เป็นอะไร 
#### Example 
```dart
void main() {
  String name = "John";
  int age = 30;
  print(name);
  print(age);
}
```
- Output
  
``` dart
John
30
```
จากตัวอย่างจะเป็นการกำหนดประเภทข้อมูลไว้แล้ว String กับ int  

## Type Inference
คือเป็นการปล่อยให้ตัว Dart จัดการเรื่อง type ว่าตัวแปร ฟังก์ชัน วัตถุ ให้เองโดยอัตโนมัติ
โดยที่ compiler สามารถรู้ type ของข้อมูลได้โดยดูจาก literal หรือค่าคงที่ที่กำหนดให้กับตัวแปร
#### Example 
```dart
void main() {
  var name = " John"; 
  var age = 30;
  print(name);
  print(age);
}
```
- Output
  
``` dart
John
30
จากตัวอย่างจะมีการกำหนดประเภทข้อมูลเป็น var คือตัวแปรที่ไม่ระบุชนิดข้อมูลตอนประกาศตัวแปร และจะสามารรู้ประเภทข้อมูลได้ตอนที่เรากำหนดค่า
