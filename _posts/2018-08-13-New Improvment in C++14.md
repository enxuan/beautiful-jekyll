---
layout: post
title: C++14 feature improvement
subtitle: C++14, feature improvement
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [C++14]
---
### C++14 improvement
* Phân tách trong số giúp đọc số dễ dàng hơn. EX: long i = 10'000'000; 
* Hỗ trợ số nhị phân trong code. Với C++11, chúng ta phải sử dụng số hexa. EX: int i = 0b1001'0001;
* Kiểu trả về của function có thể là auto và được xác định kiểu tại compiler time. EX: auto max(int a, int b);
* constexpr function: function mà được tính toán giá trị trở về tại compiler time, giúp chương trình chạy mượt hơn vì không phải tính toán tại runtime.
* Hỗ trợ variable template. EX: 
