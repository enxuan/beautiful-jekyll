---
layout: post
title: C++ Const using purpose
subtitle: C++ sử dụng constand keyword
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [C++ const, c++ hằng]
---
Sử dụng const cho biến:  
int const PI = 3.14; // Khai báo biến PI = 3.14 và biến này không thể thay đổi giá trị trong suốt chương trình

trong hàm:  
int function(int const& i) //Khai báo biến i được truyền vào theo reference và gía trị biến này sẽ không thay đổi trong hàm. Khi truyền biến theo
reference, khi chạy chúng ta ko phải qua bước copy giá trị biến vào hàm, điều này làm giảm thời gian chạy chương trình và rất hiệu quả trong
việc truyền biến chiếm nhiều bộ nhớ (các lớp phức tạp có nhiều biến thành phần, ...).

Trong lớp:  
Với các hàm thành phần của lớp, nếu hàm không thay đổi giá trị của biến thành phần, hàm nên được thêm const.  
string getname() const // thể hiện hàm ko thay đổi giá trị của biến thành phần và hàm có thể được sử dụng trong các const function khác.

Trong pointer:  
Với pointer, const có các ý nghĩa sau, phụ thuộc vào vị trí của từ khoá const và dấu \"\*\"  

* int const \*pt; // pointer to a const - pt là con trỏ tới một hằng số và chúng ta không thể thay đổi giá trị của \*pt  
  \*pt = 7; // không hợp lệ vì không thể thay đổi giá trị của \*pt  
  pt = &j; // hợp lệ vì chúng ta chỉ không thể thay đổi giá trị của \*pt nên chúng ta có thể thay đổi địa chỉ pt trỏ tới
  
* int \* const pt; // const pointer - pt là con trỏ trỏ tới một địa chỉ cố định và không thể thay đổi địa chỉ này  
  \*pt = 10; // hợp lệ vì chúng ta chỉ không thể thay đổi địa chỉ pt trỏ tới vậy nên chúng ta vẫn có thể thay đổi giá trị của \*pt  
  pt = &j; //không hợp lệ vì chúng ta không thể thay đổi địa chỉ pt trỏ tới
  
* int const \* const pt; // const pointer to a const -  ta không thể thay đổi địa chỉ pt trỏ tới cũng như không thể thay đổi \*pt
