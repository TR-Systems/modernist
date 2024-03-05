---
title: Modernist Theme for GitHub Pages by TR-Systems
---

<div class="grid-toc">
<div class="grid-toc-content">
<div class="dropdown">
<button onclick="menuClick()" class="dropbtn">Table of Contents</button>
<div id="myDropdown" class="dropdown-content">
<a href="#test-on-windows">Test On Windows</a>
<a href="#test-on-raspberry-pi">Test On Ras Pi</a>
<a href="#design-elements">Design Elements</a>
<a href="#technical-details">Technical Details</a>
<a href="/test.html">Test Page</a>
</div>
</div>
<h2>{{ page.title }}</h2>
</div>
</div>


### Under Perpetual Construction and Testing!
I am using this as a learning tool for developing and testing changes for my [TR-Systems site](https://tr-systems.github.io/web/){:target="_blank"}. Feel free to grab it and go. To do so, open my [Public Template Repository](https://github.com/tr-systems/modernist){:target="_blank"}  on GitHub.

This design started out by copying the GitHub Pages Modernist Theme, which [looks like this](https://pages-themes.github.io/modernist/){:target="_blank"}.

### Recent Updates

| **24-02-28** | New grid styles! Check it out on the [Test Page!](test.md)
| **24-03-01** | Easy to code drop-down **Table of Contents** or **Link Menu** button.
| **24-03-03** | Major overhaul of Header to simplify the style sheet and improve viewing on small screens.
| **24-03-05** | **Now fully optimized for small screen viewing!**

### Usage
Good for static display of system documentation and other articles of interest. Navigation is through the home page, which I will be improving upon as time, other interests and the seasons dictate.

### Use This Template
Open this repository on GitHub and then click the green button in the upper right to ***Use this template***, ***Create new Repository*** and ***Include all Branches***. Give your repo a web friendly name like "web" or "mycoolthing" since the repo name is the top level path in the URL for your website.

### Use a Team/Pro Account
Even as a total newbie to GitHub, I recommend this low-cost option so you can use a custom domain name and publish from a private repo in a separate Team account (e.g TR-Systems), instead of publishing from a public repo on your personal account.

### Make it Your Own
ALL YOU NEED TO DO is **edit _config.yml, index, about and readme.md** to make it your own. And if you're like me and never really done this kind of thing before, open those files in the editor to see just how easy it is to use GitHub markdown formatting for your content. 

There are only a few other simple things you need to do in order to publish your web site, and that's where [GitHub Pages Help](https://docs.github.com/en/pages){:target="_blank"} and [Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github){:target="_blank"} comes in handy. All of GitHub is very well documented in their Help pages. GitHub for Dummies helped me out in the very beginning, too.

### Editing and Publishing
The repo has two branches. Apply changes and new content to the top level "edit" branch, then pull them down into the "publish" branch for the automatic "pages build" process. There may be a better way but this works for me since I've been doing all editing online up to this point. More on that below.

### Google Analytics
**Google Analytics is configured on this site for the GA stream "tr-systems.github.io/modernist/"** by using an **if** statement in **_layouts/default.html** that you will need to update or remove, along with the **include** statement and the GA snippet file for tr-systems in the **_includes** folder.

### Getting Started
[GitHub Pages Help](https://docs.github.com/en/pages){:target="_blank"}. I spent hours studying this material. I'm trying to make this so you don't really have to, *once you understand what a pull request is all about, that is. :)*

---

## Test on Windows
*Last updated: 2024-02-22*

1. Install [Git Bash](https://gitforwindows.org/){:target="_blank"} and [GitHub Desktop for Windows](https://desktop.github.com/){:target="_blank"} (all good)<br>
Git has many install options. Take the defaults but do not include *Scalar support for Large Repositories*.
2. Install [Ruby](https://rubyinstaller.org/){:target="_blank"} (all good).<br>
Take the defaults and be sure to run the ridk process at the end. I installed Ruby at c:\Ruby32. This app is huge.
3. Open Command Prompt or Git Bash and confirm:
```
ruby -v returns Ruby 3.2.3 (2024-01-18 revision 52bb2ac0a6) x64-mingw-ucrt<br>
gem -v returns 3.4.19
bundle -v returns Bundler version 2.5.6
jekyll -v returns jekyll 4.3.3
```
4. Clone the top level edit branch of the modernist repo using GitHub Desktop
5. Add **.gitignore** file to modernist root
```
_site
_posts
Gemfile
Gemfile.lock
.sass-cache
.jekyll-cache
.jekyll-metadata
vendor
```
5. Add **Gemfile** to modernist root:
```
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
gem "webrick"
gem "wdm"
```
6. Open Git Bash and switch to modernist root (edit branch)
7. Run **bundle install**<br>
Ok, 98 gems installed, a brick of web I guess.
8. Run **bundle exec jekyll serve**
9. **Error:** jekyll 3.9.5 | File to import not found or unreadable: **tr-systems-modernist**.

**@import** in **assets/css/style.scss** is simply not working locally. This issue has been posted on the [GitHub Community](https://github.com/orgs/community/discussions/108932){:target="_blank"} and [Jekyll Talk](https://talk.jekyllrb.com/t/error-file-to-import-not-found-or-unreadable-style-sheet/8973){:target="_blank"}, knowing that Jekyll on Windows is *not officially supported*.

### Workaround For Now
Copy the *contents* of the **dropdown**, **rouge-github** and **tr-systems-modernist** style sheets in **_sass** and paste them into **assets/css/style.scss**, *starting at and replacing the import statement, leaving the first 3 lines of front matter, and removing the import for rouge from tr-systems-modernist*, so **style.scss** it looks like this:

```
---
---

/* Modernist Theme for GitHub Pages by TR-Systems */
html {
... remainder of tr-systems-modernist.scss

/* Dropdown Link Button for TOC or NAV */
... all of dropdown

/* Default GitHub Code Highlighter */
... all of rouge-github or rouge-base16-dark if you want to try it.
```

1. Run **bundle exec jekyll serve**<br>
The site now builds. See it here: http://localhost:4000
2. You can now make content and style changes ***on the fly*** with the jekyll server running.
3. When you're done, copy any changes you've made to **style.scss** into **tr-systems-modernist**.
4. Push your content and style changes  up to the edit branch on GitHub using Git or GitHub Desktop, but DO NOT PUSH **style.scss**!
5. Then, on GitHub, create a pull request into the publish branch for "pages build and deploy".
6. Voila, websites made easy. Ha!

---

## Test on Raspberry Pi
2-20-24: Ok, here we go, starting with a fresh Ras pi 4 B.

1. Install Ruby and Jekyll per the doc referenced above and confirm:<br>
ruby -v returns 3.1.2p20<br>
jekyll -v returns 4.3.3
2. Cd to local **github** folder and run **git clone 'url to modernist repo'**
3. Add **.gitignore** file to repo root as above for Windows
4. Add **Gemfile** to modernist root, without "wdm"
```
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
gem "webrick"
```
5. Cd to **modernist** and run **git fetch** to get some changes between step 2 and now
6. **sudo su**
7. Run **bundle add webrick**<br>
Adds a LOT of Jekyll gems, themes and other web stuff, a brick of web I guess.
8. **exit** out of su
9. Run **bundle install**<br>
Ok, 97 gems now installed (one less than Windows, no wdm)
11. Run **bundle exec jekyll serve**
12. Yay! It works! 

FINALLY, for the first time in this never ending all time consuming silly winter project of mine, something actually worked on the first attempt! Without a single rat hole to chase down first.

---
## Design Elements
I am using the [CSS Reference](https://www.w3schools.com/cssref/index.php){:target="blank"} and more from W3Schools to learn how to be stylish.

### Media Screen Styles
Fully customized for viewing on small screens by reducing font sizes, header sizes, bottom margins and left/right page margins for all content. All grids with two columns are reset to one column.

### Media Print Style
Removes link buttons from header and toc/menu buttons from content. Also removes first two lines of footer, controlled in **default.html** by using "<p class=noprint>".

### List Item Spacing
Lists with a little space between. Easy to find and adjust in the style sheet.

1. numbered list with break<br>
more text
2. two
3. three

* bullet list with break<br>
more text
* next bullet
    * four spaces to get nested bullet with break<br>
    and more text
    * and one more
    * last nested bullet
* last one

### Color Scheme and Table Style
W3Schools helped me with the table design. The colors are shown using small image files that I created from screen shots on [color sites](https://www.color-hex.com/){:target="_blank"}. There is a better way, and I will find it, but not a priority.

| Selector | Background Colors | Color1 | Color2 |
| -------- | ----------------- | ------ | ------ |
| html | background: #6C7989; | <img class="img-raw" width="48" src="assets/images/color-6C7989.png"> | x |
| html | background: linear-gradient(#6C7989, #434B55) | <img class="img-raw" width="48" src="assets/images/color-6C7989.png"> | <img class="img-raw" width="48" src="assets/images/color-434B55.png"> |
| header | background: #C6EAFA; | <img class="img-raw" width="48" src="assets/images/color-C6EAFA.png"> | x |
| header | background: linear-gradient(#DDFBFC, #C6EAFA); | <img class="img-raw" width="48" src="assets/images/color-DDFBFC.png"> | <img class="img-raw" width="48" src="assets/images/color-C6EAFA.png"> |
| header | border-bottom:2px solid #B2D2E1; | <img class="img-raw" width="48" src="assets/images/color-B2D2E1.png"> | x |
| header: ul: before: | background:rgba(#000, 0.1); | Light Gray | x |
| header: ul: | background: #5198DF; | <img class="img-raw" width="48" src="assets/images/color-5198DF.png"> | x |
| header: ul: | background: linear-gradient(#77B9FB, #3782CD); | <img class="img-raw" width="48" src="assets/images/color-77B9FB.png"> | <img class="img-raw" width="48" src="assets/images/color-3782CD.png"> |
| section | background:#FFFFFF; | WHITE | x |
| th | background-color: #3782CD; | <img class="img-raw" width="48" src="assets/images/color-3782CD.png"> | x |


#### Java code with highlighting by **rouge-github.scss**.

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

#### Groovy code

```groovy
    errcd = "OK"
    for (feature in MotionFeatures) {
        if (filter == "" || filter.contains("$feature.key")) {
            if (device.currentValue("$feature.value") != "NA") {
                errcd = SetFeatureState("$feature.value",newstate)
                if (errcd != "OK") {break}
            } else {
                if (filter.contains("$feature.key")) {log.info "Requested feature *$feature.key* is NA"}
            }
        }
    }
```

#### Blockquote

> blockquote text with break<br>more text
>
> second paragraph

#### Definition List

Style Sheet
: Lets people know  how stylish you are

Wrapper (Generic Term)
: Used to encapsulate content on a web page

HTML/CSS Grids
: Used to encapsulate content on a web page in a defined pattern of columns, rows and cells.

# Test Header1
content
## Test Header2
content
### Test Header3
content
#### Test Header4
content
##### Test Header5
content
###### Test Header65
content
## Technical Details
**_layouts/default.html** is used to build the header and footer. **Custom local variables in _config.yml** provide the content. Link buttons will not be displayed if they are not configured.

**_sass/tr-systems-modernist.scss** is the primary style sheet, substantially modified from the original.

**_sass/dropdown.scss** provides styling for the links button, the basics of which were obtained from W3Schools and then styled to match the theme here.

**_sass/rouge-github.scss** is the default Rouge style sheet used in GitHub for code highlighting, replacing **rouge-base16-dark** that came with the original, which I have left in the **_sass** folder.

**assets/css/style.scss** is the **site style sheet**, which imports **tr-systems**, which imports **dropdown** and **rouge**.

**Note:** If you change the name of the site style sheet, you need to update the reference in **default.html**.

---

End of Document
