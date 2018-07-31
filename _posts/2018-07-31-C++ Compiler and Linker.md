---
layout: post
title: C++ Compiler và Linker
subtitle: C++ Compiler và Linker
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [C++ complier, linker]
---

Khi chúng ta viết chương trình C++ và build, trình biên dịch sẽ build mỗi file source thành 1 file object khác nhau.  
Khi chúng ta thay đổi code trong 1 file nào đó, chỉ file bị thay đổi sẽ được biên dịch lại, các file không bị thay đổi sẽ không được build lại.
Điều này làm giảm thời gian biên dịch và có thể thấy rõ hiệu quả trong các dự án lớn.  
 Nếu biên dịch bị lỗi, đầu của mỗi lỗi sẽ có chữ **C**
 
Nếu chương trình của chúng ta có nhiều file, mỗi file object khác nhau này sẽ được liên kết lại bằng linker  
 Nếu quá trình liên kết bị lỗi, đầu của lỗi sẽ có chữ **LNK**
 Quá trình liên kết file thường bị lỗi do:
 * Quên define hàm đã được khai báo trong file header và hàm này đã được gọi ở đâu đó trong code.
 * Hai file dùng và khai báo hàm không được link với nhau
