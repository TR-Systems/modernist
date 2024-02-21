## Modernist Design for GitHub Pages by [TR-Systems](https://TR-Systems.github.io/web/){:target="_blank"}
### Under Construction and Testing! (February 2024)
I am new to GitHub and using this as a learning tool and for developing and testing changes for my tr-systems site. At some point, this may become static and I may move on to a more complex design, with a different starting point.

This design started out by copying the design of the built-in [GitHub Pages Modernist Theme (opens the public repo)](https://github.com/pages-themes/modernist){:target="_blank"}, which [looks like this](https://pages-themes.github.io/modernist/){:target="_blank"}.

Click the link above to open the **public template repository** for this website design on GitHub.

### Usage
Good for static display of system documentation and articles of interest on full screen browsers. Navigation is through the home page, thus the home page button on every page header. This page (index.md) is your home page.

### Use This Template
Open TR-Systems/modernist repository on GitHub and then click the green button in the upper right to ***Use this template***, ***Create new Repository*** and ***Include all Branches***. Give your repo a web friendly name like "web" or "mycoolthing" since the repo name is the top level path in the URL for your website.

### Use a Team/Pro Account
Even as a total newbie to GitHub, I recommend this low-cost option so you can use a custom domain name and publish from a private repo in a separate Team account (e.g TR-Systems), instead of publishing from a public repo on your personal account.

### Modifications
I only copied what was needed and then modified the style sheet, default html and config to get what you see here. I removed a lot of formatting and fluff that I didn't like from the overloaded style sheet (too many cooks in the kitchen).

### Editing and Publishing
The repo has two branches. Apply changes and new content to the top level "edit" branch, then pull them down into the "publish" branch for the automatic "pages build" process. There may be a better way but this works for me since I've been doing all editing online up to this point. More on that below.

### Make it Your Own
ALL YOU NEED TO DO is **edit _config.yml, index, about and readme.md** to make it your own. And if you're like me and never really done this kind of thing before, open those files in the editor to see just how easy it is to use GitHub markdown formatting for your content. 

There are only a few other simple things you need to do in order to publish your web site, and that's where [GitHub Pages Help](https://docs.github.com/en/pages){:target="_blank"} and [Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github){:target="_blank"} comes in handy. All of GitHub is very well documented in their Help pages. GitHub for Dummies helped me out in the very beginning, too.

### Table Layout
I am using the [CSS Reference](https://www.w3schools.com/cssref/index.php){:target="blank"} from W3Schools to learn how to be stylish. And since my system doc uses tables, W3Schools showed me the way, as you see below and in the style sheet.

### List Item Spacing
I use a lot of bulleted and numbered lists in my doc and like a little space between each item, so that's something I added to the style sheet.

### Color Scheme
Same as the original. Changing it may require changing the color of elements within (i.e text colors, black or white). Linear-gradient will be used if the browser supports it otherwise it will use the solid color specified.

The colors are shown using small image files that I created from screen shots on [color sites](https://www.color-hex.com/){:target="_blank"}. There is a better way, and I will find it.

| Selector | Background Colors | Color1 | Color2 |
| -------- | ----------------- | ------ | ------ |
| html | background: #6C7989; | <img width="48" src="assets/images/color-6C7989.png"> | x |
| html | background: linear-gradient(#6C7989, #434B55) | <img width="48" src="assets/images/color-6C7989.png"> | <img width="48" src="assets/images/color-434B55.png"> |
| header | background: #C6EAFA; | <img width="48" src="assets/images/color-C6EAFA.png"> | x |
| header | background: linear-gradient(#DDFBFC, #C6EAFA); | <img width="48" src="assets/images/color-DDFBFC.png"> | <img width="48" src="assets/images/color-C6EAFA.png"> |
| header | border-bottom:2px solid #B2D2E1; | <img width="48" src="assets/images/color-B2D2E1.png"> | x |
| header: ul: before: | background:rgba(#000, 0.1); | Light Gray | x |
| header: ul: | background: #5198DF; | <img width="48" src="assets/images/color-5198DF.png"> | x |
| header: ul: | background: linear-gradient(#77B9FB, #3782CD); | <img width="48" src="assets/images/color-77B9FB.png"> | <img width="48" src="assets/images/color-3782CD.png"> |
| section | background:#FFFFFF; | WHITE | x |
| th | background-color: #3782CD; | <img width="48" src="assets/images/color-3782CD.png"> | x |

## Google Analytics
**Google Analytics is configured on this site for the GA streeam "tr-systems.github.io/modernist/"**.

PLEASE REMOVE THE INCLUDE STATEMENT FROM THE DEFAUL HTML file before publishing your site.

Then, after you get your own GA account set up for your stream, update the code in the google-analytics file and put the include back.

## Test on Windows
<small><em>Last updated: 2024-02-19 11:30am</em></small>

Still trying to clone, edit and test locally on Windows, without success. Here is the last approach I used:

1. Install Git and GitHub Desktop (all good)
2. Install Ruby and Jekyll per the [GitHub and Jekyll doc](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll){:target="_blank"} (all good).
3. Clone the repo using GitHub Desktop
4. Add **Gemfile** to modernist root directory with these three lines:
<pre>source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
gem "webrick"</pre>
5. Add **Gemfile** to **.gitignore**
6. Run **bundle add webrick** (ok)
7. Run **bundle install** (ok)
8. Run **bundle exec jekyll serve**
9. **Error:** jekyll 3.9.5 | File to import not found or unreadable: **tr-systems-modernist**.

**@import** in **assets/css/style.scss** is simply not working for me LOCALLY.

### Workaround For Now
Copy the contents of the two style sheets in **_sass** and paste them directly **assets/css/style.scss** (replacing the import). The site now builds locally and I can make changes to style.scss on the fly for quick fire testing of style changes. But I can't push style.scss back up to GitHub so I have to make the identical changes in tr-systems-modernist, which is a pain.

I have posted this problem on the [GitHub Community](https://github.com/orgs/community/discussions/108932){:target="_blank"} and [Jekyll Talk](https://talk.jekyllrb.com/t/error-file-to-import-not-found-or-unreadable-style-sheet/8973){:target="_blank"}.

## Test and Develop on Raspberry Pi 4 B
2-20-24: Ok, here we go, starting with a fresh ras pi.

1. Install Ruby and Jekyll per the doc referenced above and confirm:<br>
ruby -v returns 3.1.2p20<br>
jekyll -v returns 4.3.3
2. Cd to local **github** folder and run **git clone 'url to modernist repo'**
3. Create and save **Gemfile** to repo root and **.gitignore** as above for Windows
4. Cd to **modernist** and run **git fetch** to get some changes between step 2 and now
5. **sudo su**
7. Run **bundle add webrick**<br>
Adds a LOT of Jekyll gems, themes and other web stuff, a brick of web I guess.
8. **exit** out of su
9. Run **bundle install**<br>
Ok, 97 gems now installed (same as on Windows)
10. Run **bundle exec jekyll serve**
11. Yay! It works! 

FINALLY, for the first time in this never ending all time consuming silly winter project of mine, something actually worked on the first attempt! Without a single rat hole to chase down first.

Good time to take a good long break and get outside.

#### Catch you later...
Tis all for now. Hope someone out there finds this design useful and lets me know. That would make my day.

Thanks for checking it out.

# Test Header1
paragraph text

Some Java code with highlighting by **rouge-github.scss**.

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

1. numbered list with break<br>
more text
2. list2
3. list3

* bullet list with break<br>
more text
* next bullet
    * four spaces to get nested bullet with break<br>
    and more text
    * and one more
    * last nested bullet
* last one

Definition List (dl)
: HTML/CSS Tag: **dl**

Definition Term
: HTML/CSS Tag: **dt**

Definition Description
: HTML/CSS Tag: **dd**

> blockquote text with break<br>more text
>
> second paragraph

## Test Header2 with horizontal line (hr) below
***
some test
### Test Header3
content
#### Test Header4
content
##### Test Header5
content
## Technical Details
**_layouts/default.html** is used to build the header and footer and is substantially modified from the original. All content in the header and footer is supplied by **custom local variables in _config.yml**. 

In there are two optional link buttons in the upper right corner of the header. If not configured, they will not be displayed. Since nav is currently through the home page, that link is on all pages. The default html file controls that and the style sheet controls how the buttons are placed and squeezed together, with a 6px gray border around them. Rather tricky. *So don't mess with the header section of the style sheet!* Actually, have at it. It's always fun to play around and learn new things in the process. That's the whole point of this for me.

**_sass/tr-systems-modernist.scss** is the style sheet and since it was developed and modified over years in the public domain, it was disorganized and hard to follow so I am still in the process of cleaning it up by first learning what everything does and then keeping only those mods and adding others to suit my style, which I then apply to my tr-systems site. So just grab it and go.

**_sass/rouge-github.scss** is the default Rouge style sheet used in GitHub for code highlighting, replacing **rouge-base16-dark** that came with the original, which I have left in the **_sass** folder. I also removed all of the custom styling of **code** and **pre** elements from the original, so I can start with html defaults and take it from there.

**assets/css/style.scss** is used to import the **tr-systems-modernist** style sheet for inclusion in the site, which then imports rouge-github.

### @Media Print, Screen Styles
I've only begun to explore. Current style settings are all original but definitely needs changes since I widened the content section substantially. It's in here that you can make it smaller/better for tablets and phones (e.g. smaller fonts, much smaller h1 h2 headings, etc.). Tables like that shown above will be a problem on small screens.

End of Document
