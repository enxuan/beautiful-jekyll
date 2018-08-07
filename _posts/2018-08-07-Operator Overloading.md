---
layout: post
title: C++ Operator Overloading
subtitle: C++ Operator 
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [C++ operator overloading, ghi đè toán tử]
---
### Giới Thiệu
Với những kiểu dữ liệu mặc định như int, double, char, chúng ta thường dùng các toán tử quen thuộc như +, _, *, /,...

Chúng ta đã quen với các toán tử tự nhiên này nên việc sử dụng chúng rất dễ và không thể nhầm được như khi chúng ta dùng các tên hàm tương tự như add, subtraction, multiple, ...

C++ có cơ chế hỗ trợ chúng ta dùng các toán tử này với các lớp chúng ta tự viết, cơ chế này được gọi là _Operator Overloading_

### Cách dùng

Khai báo:
* Với class member function:  
 <kiểu dữ liệu trả về> <Class name>::operator<operator sign> (<other type> <param name>)  
  EX: bool MyClass::operator<(int i);  
  Using:  
    MyClass a1;  
    bool b = a1 < 10;  
* Với hàm tự do:  
 <kiểu dữ liệu trả về> operator<operator sign>(<other type> <param 1>, <your class> <param 2>)  
 EX bool operator<(int i, MyClass a);  
  Using:  
    MyClass a1;  
    bool b = i < a1;  
   
> Chú ý
Với member class function, chúng ta có thể truy cập các biến private nhưng với hàm tự do, chúng ta không thể truy cập các biến private này
Khi chúng ta viết operator với hàm tự do cần dùng tới private member  của class, chúng ta có thể có những cách sau:
>* Khai báo hàm pulic để lấy giá trị cần sử dụng ví dụ: getName, getID, .. và sử dụng các hàm get này trong hàm tự do.
 Nhược điểm: mất tính đóng gói dữ liệu mà chúng ta đã thiết kế trước đó
>* Khai báo hàm tự do là friend function của lớp, cách này sẽ không phá vỡ cấu trúc của lớp chúng ta thiết kế là có thể sử dụng tới private member variable
