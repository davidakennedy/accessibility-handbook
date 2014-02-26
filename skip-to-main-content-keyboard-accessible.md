---
layout: page
title:  "Skip to Main Content - Keyboard Accessible"
date: 2014-02-26
last_updated: 2014-02-26
---

HTML
```html
<ul>
    <li><a href="#">Nav Item 1</a></li>
    <li><a href="#">Nav Item 2</a></li>
    <li><a href="#">Nav Item 3</a></li>
    <li><a href="#">Nav Item 4</a></li>
</ul>

```css
a.skip-main {
    left:-999px;
    position:absolute;
    top:auto;
    width:1px;
    height:1px;
    overflow:scroll;
    z-index:-999;
}
a.skip-main:focus, a.skip-main:active {
    color: #fff;
    background-color:#000;
    left: auto;
    top: auto;
    width: 30%;
    height: auto;
    overflow:auto;
    margin: 10px 35%;
    padding:5px;
    border-radius: 15px;
    border:4px solid yellow;
    text-align:center;
    font-size:1.2em;
    z-index:999;
}
```

<p id="main">This is the main content. In this example you will note that the &quot;Skip to main content&quot; link appears when I tab through the page. This allows keyboard-only users, in addition to screen reader users, an easy way to skip repetitive navigation. The key components to implementing this are</p>
```
1. Provide a link at the top of the page that says &quot;skip to main content&quot;
2. Have it link to an internal anchor further down in the page where the main content begins.
3. Use CSS :focus and :activate to make the skip link visible when the user tabs to it
