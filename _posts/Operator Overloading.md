---
layout: post
title: C++ Compiler và Linker
subtitle: C++ Compiler và Linker
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
  
