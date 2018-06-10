---
title: How to create new page
date: 2018-06-04 19:37:45
tags: hexo new page pages generate
---
## Basics
### 3 types of Pages:
* Post
 * Post is like news
 `hexo new Hello world!`
* Draft
 * Draft unpublished news
 `hexo new draft Second hidden hello world!`
 * Make it published:
 `hexo publish Second hidden hello world!`
* Pages
 * Menu like pages
 `hexo new page About`

### Examples:
This is path in console where it create new page
![create new pages](./../../../../images/create new pages.png "create new page")
`hexo generate`
![create new pages](./../../../../images/create new pages1.png "create new page")
Going in this folder and putting resources.
using folder `www/2018/06/04/page/your resources here`  the path you will need to put like `./images/fork.png` for all your resources like images etc
or using `www` folder the path you will need to put like `./../../../../images/fork.png`
```ruby
![random image](./../../../../images/2018-www.png "random image")
```
![fork repository](./../../../../images/2018-www.png "fork it")
