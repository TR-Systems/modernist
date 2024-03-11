---
title: Style Sheet Test Page
---

<div class="dropdown">
<button onclick="buttonClick()" class="dropbtn">Table of Contents</button>
<div id="myDropdown" class="dropdown-content">
<a href="#toc-made-easy">TOC Made Easy</a>
<a href="#grid-styles">Grid Styles</a>
<a href="#50-50-grid">50-50 Grid</a>
<a href="#66-33-grid">66-33 Grid</a>
<a href="#pipe-testing">Pipe Testing</a>
<a href="#table-testing">Table Testing</a>
</div>
<h3>{{ page.title }}</h3>
</div>

Use this page to see just how stylish you can be...

#### KBD Testing
Press <kbd>Ctrl</kbd> + <kbd>c</kbd>

```
Press <kbd>Ctrl</kbd> + <kbd>c</kbd>
```

#### Picture Testing
Use one of the custom **image classes** to to create a picture frame or round over the corners:

```
<img width="20%" src="assets/images/zion-np.jpg">
 <img class="img-noborder" width="20%" src="assets/images/zion-np.jpg">
 <img class="img-border2" width="20%" src="assets/images/zion-np.jpg">
 <img class="img-border4" width="20%" src="assets/images/zion-np.jpg">
```

<img width="20%" src="assets/images/zion-np.jpg">
 <img class="img-noborder" width="20%" src="assets/images/zion-np.jpg">
 <img class="img-border2" width="20%" src="assets/images/zion-np.jpg">
 <img class="img-border4" width="20%" src="assets/images/zion-np.jpg">

---

### TOC Made Easy
Use this at the start of each page that warrants it.

```
---
title: Style Sheet Test Page
---

<div class="dropdown">
<button onclick="buttonClick()" class="dropbtn">Table of Contents</button>
<div id="myDropdown" class="dropdown-content">
<a href="#grid-styles">Grid Styles</a>
<a href="#toc-made-easy">TOC Made Easy</a>
<a href="#50-50-grid">50-50 Grid</a>
<a href="#66-33-grid">66-33 Grid</a>
<a href="#pipe-testing">Pipe Testing</a>
<a href="#table-testing">Table Testing</a>
</div>
<h3>{{ page.title }}</h3>
</div>
```

---

### Grid Styles
Placing text and other content next to an image can be done in several ways and gets really complicated really fast, but I got his working with a custom grid classes in the style sheet and html in the markdown. This appears to be the only way to create a grid out of markdown. You will see how when you edit **test.md**.

You can run wild with these, provided you don't mind editing raw html in your pages, which is prone to the slightest slip or miss that makes your web page run wild, too.

But it works and it ain't that hard. Easy to copy/paste the basic structure needed and then fill in the content.

### 50-50 Grid
Each element in the grid starts with a horizontal rule that spans the width of the column, with a 32px gap.

Other grid classes include **grid-6633 and grid-3366**. Like I said, you can run wild.

<div class="grid-5050">
<div class="grid-c1">
<hr>
<h4>First Element in the Grid</h4>
<p>With image width=50%</p>
<img width="50%" class="img-border2" src="assets/images/zion-np.jpg">
</div>
<div class="grid-c2">
<hr>
<h4>Second Element</h4>
<hr>
<p>Virgin River - Zion National Park</p>
<hr>
<p>800x600 image resized to fit 50% of the grid column.</p>
</div>
<div class="grid-c1">
<hr>
<h4>Third Element</h4>
<p>Formatted text. Code highlighting doesn't work here.</p>
<pre>
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
</pre>
</div>
<div class="grid-c2">
<hr>
<h4>Fourth Element</h4>
<p>More content</p>
</div>
</div>

Next markdown paragraph after the grid.

---

### 66-33 Grid

<div class="grid-6633">
<div class="grid-c1">
<hr>
<h4>First Element in the Grid</h4>
<p>With image width=66%</p>
<img width="66%" class="img-noborder" src="assets/images/zion-np.jpg">
</div>
<div class="grid-c2">
<hr>
<h4>Second Element</h4>
<hr>
<p>Virgin River - Zion National Park</p>
<hr>
</div>
</div>

Next markdown paragraph after the grid.

---

### Pipe Testing
Using the Pipe/Vertical Bar Symbol yields table cells

| One pipe, one table data cell

| Two pipes with image after the second  | <img class="img-border2" width="160" src="assets/images/zion-np.jpg">

---

### Table Testing
Trying to fill a table data cell with a background color.

| Hex Code | Color |
| -------- | ----- |
| #6C7989 | <span style="font-size:36px;height:36px;width:36px;background:#6C7989;"> x </span> |
| next | next |

---

Fun stuff...

---

End of Document
