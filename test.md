---
title: Style Sheet Test Page
---

<div class="grid-toc">
<div class="grid-toc-content">
<div class="dropdown">
<button onclick="myFunction()" class="dropbtn">Table of Contents</button>
<div id="myDropdown" class="dropdown-content">
<a href="#grid-styles">Grid Styles</a>
<a href="#toc-made-easy">TOC Made Easy</a>
<a href="#50-50-grid">50-50 Grid</a>
<a href="#66-33-grid">66-33 Grid</a>
<a href="#pipe-testing">Pipe Testing</a>
<a href="#table-testing">Table Testing</a>
</div>
</div>
<h2>{{ page.title }}</h2>
</div>
</div>

### KBD Testing
Press <kbd>Ctrl</kbd> + <kbd>c</kbd>

```
Press <kbd>Ctrl</kbd> + <kbd>c</kbd>
```

### Picture Testing
By default for the **img** tag, the style sheet creates a *picture frame* with 4px of padding and 4px of rounded border, for a total increase in width and height of 16px, which you can over-ride by using one of the other image styles:

```
<img width="20%" src="assets/images/zion-np.jpg" alt="Zion National Park">
 <img class="img-border2" width="20%" src="assets/images/zion-np.jpg">
 <img class="img-noborder" width="20%" src="assets/images/zion-np.jpg">
 <img class="img-raw" width="200" src="assets/images/zion-np.jpg">
```

<img width="20%" src="assets/images/zion-np.jpg" alt="Zion National Park">
 <img class="img-border2" width="20%" src="assets/images/zion-np.jpg">
 <img class="img-noborder" width="20%" src="assets/images/zion-np.jpg">
 <img class="img-raw" width="200" src="assets/images/zion-np.jpg">

---

### Grid Styles
Placing text and other content next to an image can be done in several ways and gets really complicated really fast, but I got his working with a custom grid class in the style sheet and html in the markdown. This appears to be the only way to create a grid out of markdown.

You can run wild with these, so I'm providing four that you can use out of the box, provided you don't mind editing raw html in your pages, which is prone to the slightest slip or miss that makes your web page run wild, too.

But it works and it ain't that hard. Easy to copy/paste the basic structure needed and then fill in the content.

Grid classes "grid-c1" and "grid-c2" allows you to define styles for the elements in each column separately, if you want something different from the defined style for those elements. For example, you may want smaller or larger paragraph text in one of the columns. 

On this site, the horizontal rule is resized from 6px to 3px to give it a better look in the confines of the grid.

```
When entering HTML in your MD files, leave a blank line before and after
each block of code and DO NOT INDENT html tags for clarity. Every line should
start with a <tag> and end with the terminator of that </tag> or any other tag.

<div class="grid-5050">
<div class="grid-c1">
<hr>
<h4>First Element in the Grid</h4>
</div>
<div class="grid-c2"><hr><h4>Second Element</h4></div>
<div class="grid-c1"><hr><h4>Third Element</h4></div>
</div>
```

### TOC Made Easy
Use **grid-toc** to provide a table of contents button and the **page title** at the start of each page that warrants it.  The **page title** is a critical element that goes into the meta data of your site and used by search engines. Jekyll/Liquid will use the first h1 or h2 header as the page title by default, unless you provide it in the **front matter**, which you can then reference anywhere in your markdown or html, as you will see in both **index.md and test.md** and shown here:.

```
---
title: Style Sheet Test Page
---

<div class="grid-toc">
<div class="grid-toc-content">
<div class="dropdown">
<button onclick="myFunction()" class="dropbtn">Table of Contents</button>
<div id="myDropdown" class="dropdown-content">
<a href="#grid-styles">Grid Styles</a>
<a href="#toc-made-easy">TOC Made Easy</a>
<a href="#50-50-grid">50-50 Grid</a>
<a href="#66-33-grid">66-33 Grid</a>
<a href="#pipe-testing">Pipe Testing</a>
<a href="#table-testing">Table Testing</a>
</div>
</div>
<h2>{ { page.title } }</h2> /* without space between braces */
</div>
</div>
```

### 50-50 Grid
Each element in the grid starts with a horizontal rule that spans the width of the column.

Other grid classes include **grid-6633 and grid-3366**. Like I said, you can run wild.

<div class="grid-5050">
<div class="grid-c1">
<hr>
<h4>First Element in the Grid</h4>
<img class="img-border2" src="assets/images/zion-np.jpg">
</div>


<div class="grid-c2">
<hr>
<h4>Second Element</h4>
<hr>
<p>Virgin River - Zion National Park</p>
<hr>
<p>800x600 image resized by the browser to fit the column width and using the smaller border so it doesn't intrude on the gap between columns as much.</p>
<p>Three images after this paragraph, with a space between and width=80, 100, 120.</p>
<img width="80" src="assets/images/zion-np.jpg"> 
<img width="100" src="assets/images/zion-np.jpg"> 
<img width="120" src="assets/images/zion-np.jpg">
<p>Then a new paragraph to end the content of this element.</p>
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
<p>Using img-noborder.</p>
<img class="img-noborder" src="assets/images/zion-np.jpg">
</div>

<div class="grid-c2">
<hr>
<h4>Second Element</h4>
<hr>
<p>Virgin River - Zion National Park</p>
<hr>
</div>

<div class="grid-c1">
<hr>
<h4>Third Element</h4>
<pre>
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
</pre>
</div>

<div class="grid-c2">
<hr>
<h4>Images Without Borders</h4>
<img class="img-noborder" src="assets/images/zion-np.jpg">
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

| Type | Model | Firmware | Web Version | Purchased |
| ---- | ----- | -------- | ----------- | --------- |
| Outdoor Mini-Dome (4) | DS-2CD-2543-G0-IS | v5.5.61 b180718<br>v5.6.820 b220519<br>v5.6.821 b230831 | v4.0.1 b180626<br>v4.0.1 b220610 | 3 in 2018<br>1 in 2023 |
| Indoor Cube w/PIR | DS-2CD-2422-FWD-IW | v5.5.0 b170725 | v4.0.1 b170711 | 2018  |
| Outdoor PTZ Mini-Dome | DS-2DE-3404-W-DE | v5.7.4 b221130<br>v5.8.1 b231108 | v4.0.1 b220121 | 2024 |
| NVR | DS-7604-NI-Q1 | v4.32.110 b211009 | v4.0.1 b210914 | 2024 |

---

Fun stuff...

---

End of Document
