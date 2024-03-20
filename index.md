---
title: Lakeside Blues Theme for GitHub Pages by TR-Systems
print: print-button.html
toc: toc-homepage.html
---

### Under Perpetual Construction and Testing
I am using this as a learning tool for developing and testing changes for my [TR-Systems site](https://tr-systems.github.io/web/){:target="_blank"}. Feel free to grab it and go. To do so, open my [Public Template Repository](https://github.com/tr-systems/modernist){:target="_blank"}  on GitHub.

This design started out by copying the GitHub Pages Modernist Theme, which [looks like this](https://pages-themes.github.io/modernist/){:target="_blank"}.

### Recent Updates

| **24-02-28** | New grid styles! Check it out on the [Test Page!](test.md)
| **24-03-01** | Easy to code drop-down **Table of Contents** or **Link Menu** button.
| **24-03-03** | Major overhaul of body parts and styling class structure.
| **24-03-05** | **Now fully optimized for small screen viewing!**
| **24-03-13** | Scrolling content with optional **TOC in fixed header always on screen**. Optimized for **printing**.
| **24-03-17** | But wait, there's more! **Optional site menu and print buttons** in header.
| **24-03-18** | Overhaul config variables and default html for clarity and purpose. Add a bit more style.
| **24-03-18** | Now called **Lakeside Blues**, so as not to intrude or confuse. Repo name stays the same.
| **24-03-19** | New Get Started page for beginners

### Usage
Good for static display of system documentation and other articles of interest, which I will be improving upon as time, other interests and the seasons dictate.

### Use This Template
Open this repository on GitHub and then click the green button in the upper right to ***Use this template***, ***Create new Repository*** and ***DO NOT Include all Branches***. Give your repo a web friendly name like "web" or "mycoolthing" since the repo name is the top level path in the URL for your website. Then, click here to [Get Started](getstarted.html).

### Use a Team/Pro Account
Even as a total newbie to GitHub, I recommend this low-cost option so you can use a custom domain name and publish from a private repo in a separate Team account (e.g TR-Systems), instead of publishing from a public repo on your personal account.

### Make it Your Own
ALL YOU NEED TO DO is **edit _config.yml, index, about and readme.md** to make it your own. And if you're like me and never really done this kind of thing before, open those files in the editor to see just how easy it is to use GitHub markdown formatting for your content. 

There are only a few other simple things you need to do in order to publish your web site, and that's where [GitHub Pages Help](https://docs.github.com/en/pages){:target="_blank"} and [Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github){:target="_blank"} comes in handy. All of GitHub is very well documented in their Help pages. GitHub for Dummies helped me out in the very beginning, too.

### Editing and Publishing
The repo has two branches. Apply changes and new content to the top level "edit" branch, then pull them down into the "publish" branch for the automatic "pages build" process.

### Google Analytics
**Google Analytics** is configured on this site for the GA stream "**tr-systems.github.io/modernist/**" by using an **if** statement in **_layouts/default.html** that you will need to update or remove, along with the **include** statement and the GA snippet file for tr-systems in the **_includes** folder.

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

Using **@import** in **assets/css/style.scss** does not work locally on Windows. To get around this, all I  had to do was copy the the contents of the style sheets in **_sass** and paste them into **style.scss**. Then:

1. Run **bundle exec jekyll serve**<br>
The site now builds. See it here: http://localhost:4000
2. You can now make content and style changes ***on the fly*** with the jekyll server running.
3. When you're done, **push** your changes up to the **edit branch** on GitHub using Git or GitHub Desktop.
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
Fully optimized for viewing on small screens by reducing font sizes, header sizes, bottom margins and left/right page margins for all content. Grids are reset to one column. Description and logo are removed from header. Tagline is removed from footer.

### Media Print Style
Description and all link buttons are removed from header. Footer is removed.

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
The colors are shown using html "<span style=...>" in the markdown. This [color site](https://www.color-hex.com/){:target="_blank"} is a good reference.

| Color1 | Color2 | Selector |
| ------ | ------ | -------- |
| <span style="background:#6C7989;padding:2px 16px;color:white;">#6C7989</span> | <span style="background:#434B55;padding:2px 16px;color:white;">#434B55</span> | html background, footer background (color2) |
| <span style="background:#069;padding:2px 17px;color:white;">#006699</span> | | header (h1, p, li, toc-button, border}, th |
| <span style="background:#d1e5fc;padding:2px 14px;">#D1E5FC</span> | <span style="background:#b3d5fb;padding:2px 12px;">#B3D5FB</span> | header background, drop-content background |
| <span style="background:aliceblue;padding:2px 16px">aliceblue</span> | | wrapper background (content) |
| <span style="background-color:#e0eefd;padding:2px 14px">#E0EEFD</span> | | tr:even |
| <span style="background-color:white;padding:2px 28px">white</span> | | tr:hover |
| <span style="background:azure;padding:2px 28px;">azure</span> | | blockquote background |
| <span style="background:silver;padding:2px 28px">silver</span> | | border: th, td, toc-button, menu-button, footer |



### Code Highlighting
This is the default Rouge highlighter for GitHub Pages. Many other options are available.

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

#### Keyboard Keys
Press <kbd>Ctrl</kbd> + <kbd>c</kbd>

```
Press <kbd>Ctrl</kbd> + <kbd>c</kbd>
```

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
###### Test Header6
content

---

### Technical Details
#### _config.yml
Contains the variables that define all of the content in the header and footer of every page and thus is the first file you need to edit. Most of the content variables for the header and footer are optional.

#### _layouts/default.html
Defines the HTML structure of your pages and is where the values of the config variables are placed on the page.

#### assets/css/style.scss
Defines how all content appears on your pages and is referenced in the <head> section of **default.html**. Jekyll copies and renames it to **style.css** when building the site.

#### assets/images
Cut and crop your image files down in size and resolution before uploading. You can then fine-tune the size of an image on a page using width or height settings when you reference it. There is much more to this topic than I can possibly share with you here. Just don't upload full res pics from your camera.

#### _includes
This is where you will define your **site menu** for all pages and a **table of contents** for any page that warrants, which are referenced in **default.html**. The **site menu** is called out in the **config** file using the **menu** variable. A **toc** is called out in the front matter of the page using the **toc** variable.

#### print-button.html
If you want the print button to appear in the header, call it out in the front matter of your page using the **print** variable.

#### button-script.html
This is the script that displays the dropdown list for the site menu and toc buttons when clicked. Currently, it will only hide the toc content when you click elsewhere on the page. So for now, the only way to hide the site menu is to click on it again. This is a work in progress and a major change in the script and methods being used is required. Still learning. 

---

End of Document
