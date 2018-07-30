---
layout: post
title: mark down symbol
subtitle: Each post also has a subtitle
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [test]
---

Mark down symbol is like html tag to determine text's format:

**_** : Make the text inside is italic
>EX: _this is italic text_
    
****** : make the text inside is bold
>EX: **this is bold text**
    
**#** : make the header level. how many symbol will stand for which header level (one symbol: header level 1, two symbol: header level two)

###This is header level three

**Link**: these are two kind of link: _inline link_ and _reference link_  
 * **Inline Link**: [text for the link] (link page)  
    we must write exactyly the link in link page
 * **reference link**: [text for the link] [reference link]  
    you must define the reference link at the end of file with fomat: [reference link]: the page link  
   * the advantage of this kind is we can change the link page just at the end of the file, not need to change every where the link page used.

**Image**: like link, just add **!** before the link

**list**: these are two kind of list, **ordered list** and **unordered list**  
 Unordered list: push one star at the begining or line (add blank space after the star mark). Each list level is difference by one blank space
* This is list level 1
  * this is list level 2
   * this is list level 3
* Another list level 1  

 Ordered list: you add the number at the beginning of the line as you want how it show to you.
 1. this is fist list item
  * this is the sub item
  
 2. this is second list item
 3. list is third list item
