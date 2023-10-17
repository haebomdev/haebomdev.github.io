---
layout: post
title: "Markdown Syntax"
date: 2023-10-13 18:39:35 +0900
author: KDH
description: List of rare makrdown syntax
thumbnail: https://img.freepik.com/free-photo/website-html-code-browser-view-printed-white-paper-closeup-view_211682-166.jpg?w=996&t=st=1697546256~exp=1697546856~hmac=426a0b6e50c1e2c15ecd1ad8f07565743966995c58cd410e4f78ae6af9555ff5
---

# Math

$ a \* b = c ^ b $

$ 2^{\frac{n-1}{3}} $

$ \int_a^b f(x)\,dx. $

# Mermaid

```mermaid!
pie title Pets adopted by volunteers
  "Dogs" : 386
  "Cats" : 85
  "Rats" : 35
```

# Code

```py
print("hi")
```

```js
console.log("hi");
```

```c
printf("hi");
```

```java
System.out.println("hi");
```

# Imbed

## Spotify

![](http://open.spotify.com/track/4Dg5moVCTqxAb7Wr8Dq2T5)

## Youtube

![](https://www.youtube.com/watch?v=Ptk_1Dc2iPY)

![](//www.youtube.com/watch?v=Ptk_1Dc2iPY?width=800&height=500)

## Soundcloud

![](https://soundcloud.com/aviciiofficial/preview-avicii-vs-lenny)

# Table

|              Stage | Direct Products | ATP Yields |
| -----------------: | --------------: | ---------: |
|         Glycolysis |           2 ATP |            |
|                 ^^ |          2 NADH |   3--5 ATP |
| Pyruvaye oxidation |          2 NADH |      5 ATP |
|  Citric acid cycle |           2 ATP |            |
|                 ^^ |          6 NADH |     15 ATP |
|                 ^^ |          2 FADH |      3 ATP |
|         30--32 ATP |                 |            |

| : Easy Multiline : |        |           |
| :----------------- | :----- | :-------- |
| Apple              | Banana | Orange \  |
| Apple              | Banana | Orange \  |
| Apple              | Banana | Orange    |
| Apple              | Banana | Orange \  |
| Apple              | Banana | Orange    |
| Apple              | Banana | Orange    |

|--|--|--|--|--|--|--|--|
|♜| |♝|♛|♚|♝|♞|♜|
| |♟|♟|♟| |♟|♟|♟|
|♟| |♞| | | | | |
| |♗| | |♟| | | |
| | | | |♙| | | |
| | | | | |♘| | |
|♙|♙|♙|♙| |♙|♙|♙|
|♖|♘|♗|♕|♔| | |♖|

| : Fruits \|\| Food : |           |           |
| :------------------- | :-------- | :-------- |
| Apple                | : Apple : | Apple \   |
| Banana               | Banana    | Banana \  |
| Orange               | Orange    | Orange    |
| : Rowspan is 4 :     |           | How's it? |
| ^^ A. Peach          |           | 1. Fine : |
| ^^ B. Orange         |           | ^^ 2. Bad |
| ^^ C. Banana         |           | It's OK!  |

| : MathJax \|\| Image : |           |                                |
| :--------------------- | :-------- | :----------------------------- |
| Apple                  | : Apple : | Apple \                        |
| Banana                 | Banana    | Banana \                       |
| Orange                 | Orange    | Orange                         |
| : Rowspan is 4 :       |           | : How's it? :                  |
| ^^ A. Peach            |           | 1. ![example][cell-image]      |
| ^^ B. Orange           |           | ^^ 2. $I = \int \rho R^{2} dV$ |
| ^^ C. Banana           |           | **It's OK!**                   |

[cell-image]: https://jekyllrb.com/img/octojekyll.png "An exemplary image"

{:color-style: style="background: black;"}
{:color-style: style="color: white;"}
{:text-style: style="font-weight: 800; text-decoration: underline;"}

| : Here's an Inline Attribute Lists example : |                                                               |     |     |
| -------------------------------------------- | ------------------------------------------------------------- | --- | --- |
| : :                                          | : <div style="color: red;"> &lt; Normal HTML Block > </div> : |     |     |
| ^^                                           | Red {: .cls style="background: orange" }                      |     |     |
| ^^ IALs                                      | Green {: #id style="background: green; color: white" }        |     |     |
| ^^                                           | Blue {: style="background: blue; color: white" }              |     |     |
| ^^                                           | Black {: color-style text-style }                             |     |     |

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]: https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
