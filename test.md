---
title: Style Sheet Test Page
print: print-button.html
toc: toc-testpage.html
---

Use this page to see just how stylish you can be...

#### Picture Testing
Use one of the custom **image classes** to to create a picture frame or round over the corners:

```
<img width="20%" src="images/zion-np.jpg">
 <img class="img-noborder" width="20%" src="images/zion-np.jpg">
 <img class="img-border2" width="20%" src="images/zion-np.jpg">
 <img class="img-border4" width="20%" src="images/zion-np.jpg">
```

<img width="20%" src="images/zion-np.jpg">
 <img class="img-noborder" width="20%" src="images/zion-np.jpg">
 <img class="img-border2" width="20%" src="images/zion-np.jpg">
 <img class="img-border4" width="20%" src="images/zion-np.jpg">

---

### TOC Made Easy
First, create html files in the **_includes** folder that look like this. Every header in your content file will be assigned a name that you can reference with spaces in the header repaced with dashes:

```
<div class="toc">
<div class="toc-dropdown">
<button onclick="tocButtonClick()" class="toc-button">Table of Contents</button>
<div id="tocContent" class="toc-drop-content">
<a href="#toc-made-easy">TOC Made Easy</a>
<a href="#grid-styles">Grid Styles</a>
<a href="#50-50-grid">50-50 Grid</a>
<a href="#66-33-grid">66-33 Grid</a>
<a href="#pipe-testing">Pipe Testing</a>
</div>
</div>
<h3>{{ page.title }}</h3>
</div>
```

Then, put this **front matter** at the start of the markdown file for the page, with an empty line before your first line of content.

```
---
title: Style Sheet Test Page
toc: toc-testpage.html
---

```

---

### Grid Styles
Placing text and other content next to an image can be done in several ways and gets really complicated really fast, but I got his working with grid classes in the style sheet and html in the markdown. This appears to be the only way to create a grid out of markdown. You will see how when you edit **test.md**.

You can run wild with these, provided you don't mind editing raw html in your pages, which is prone to the slightest slip or miss that makes your web page run wild, too. Easy to copy/paste the basic structure needed and then fill in the content.

### 50-50 Grid
Each element in the grid starts with a horizontal rule that spans the width of the column, with a 32px gap.

Other grid classes include **grid-6633 and grid-3366**. Like I said, you can run wild.

<div class="grid-5050">
<div class="grid-c1">
<hr>
<h4>First Element in the Grid</h4>
<p>With image width=50%</p>
<img width="50%" class="img-border2" src="images/zion-np.jpg">
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
<img width="66%" class="img-noborder" src="images/zion-np.jpg">
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

| Two pipes with image after the second  | <img class="img-border2" width="160" src="images/zion-np.jpg">

---

Fun stuff...

---

End of Document
