## Modernist Theme for GitHub Pages by [TR-Systems](https://TR-Systems.github.io/web/){:target="_blank"}
### Under Construction and Testing! (February 2024)
### 2-18-24: Currently TESTING local build and serve on Windows PC and it's NOT WORKING!

Click the link above to open the public template repository for this theme on GitHub.

This theme started out by copying the design of the built-in [GitHub Pages Modernist Theme (opens the public repo)](https://github.com/pages-themes/modernist){:target="_blank"}, which [looks like this](https://pages-themes.github.io/modernist/){:target="_blank"}.

### Usage
Good for static display of system documentation and articles of interest on full screen browsers. Navigation is through the home page, thus the home page button on every page header. This page (index.md) is your home page.

### Use This Template
Open TR-Systems/modernist repository on GitHub and then click the green button in the upper right to ***Use this template***, ***Create new Repository*** and ***Include all Branches***. Give your repo a web friendly name like "web" or "mycoolthing" since the repo name is the top level path in the URL for your website.

### Use a Team/Pro Account
Even as a total newbie to GitHub, I recommend this low-cost option so you can use a custom domain name and publish from a private repo in a separate Team account (e.g TR-Systems), instead of publishing from a public repo on your personal account.

### Modifications
I only copied what was needed and then modified the style sheet, default html and config to get what you see here. I removed a lot of formatting and fluff that I didn't like from the overloaded style sheet (too many cooks in the kitchen).

### Editing and Publishing
The repo has two branches. Apply changes and new content to the top level "edit" branch, then pull them down into the "gh-pages" branch for the automatic "pages build" process. There may be a better way but this works for me since I've been doing all editing online.

Update: 2-18-24:

I am now trying to clone, edit and test locally on Windows, without success. Here are the steps I've taken to go Local on Windows 10 PC:

1. [Install Ruby and Jekyll per the GitHub Pages](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll){:target="_blank"}.
2. Clone the repo using GitHub Desktop
3. Open Git Bash and switch to the repo root directory
4. Run: **jekyll new --skip-bundle --force .** (because it's not empty)
5. Edit: Gemfile as noted above and _config.yml to suit my needs
6. Run: **bundle install** (OK)
7. Run: **bundle exec jekyll serve**
8. Error: File to import not found: **tr-systems-modernist**

[GitHub Pages help](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll){:target="_blank"} shows how to create a new site using the built-in Jekyll minima theme but it doesn't show me how to take an existing repo that builds without error on GitHub and configure it locally for testing with **Jekyll serve** on localhost:4000. So if you know how, please let me know! Thanks!

### Make it Your Own
ALL YOU NEED TO DO is **edit _config.yml, index, about and readme.md** to make it your own. And if you're like me and never really done this kind of thing before, open those files in the editor to see just how easy it is to use GitHub markdown formatting for your content. 

There are only a few other simple things you need to do in order to publish your web site, and that's where [GitHub Pages Help](https://docs.github.com/en/pages){:target="_blank"} and [Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github){:target="_blank"} comes in handy. All of GitHub is very well documented in their Help pages. GitHub for Dummies helped me out in the very beginning, too.

**_layouts/default.html** is used to build the header and footer and is substantially modified from the original. All content in the header and footer is supplied by **custom local variables in _config.yml**. 

In there are two optional link buttons in the upper right corner of the header. If not configured, they will not be displayed. Since nav is currently through the home page, that link is on all pages. The default html file controls that and the style sheet controls how the buttons are placed and squeezed together, with a 6px gray border around them. Rather tricky. *So don't mess with the header section of the style sheet!* Actually, have at it. It's always fun to play around and learn new things in the process. That's the whole point of this for me.

**_sass/modernist.scss** is the style sheet and since it was developed and modified over years in the public domain, it was disorganized and hard to follow so I am still in the process of cleaning it up by first learning what everything does and then keeping only those mods and adding others to suit my style, which I then apply to my tr-systems site. So just grab it and go.

**_sass/rouge-base16-dark.scss** is the style sheet for code highlighting. I sure won't be messing with that, other than trying to set it to the 30px left and 24px right padding defined in the section selector so it lines up with all other content. See below. 

I am still learning margins and padding and where to apply them in the style sheet to get the desired effect.

### @Media Print, Screen Styles
I've only begun to explore. Current style settings are all original but definitely needs changes since I widened the content section substantially. It's in here that you can make it smaller/better for tablets and phones (e.g. smaller fonts, much smaller h1 h2 headings, etc.). Tables like that shown below will be a problem on small screens.

### Table Layout
I am using the [CSS Reference](https://www.w3schools.com/cssref/index.php){:target="blank"} from W3Schools to learn how to be stylish. Very useful. And since my system doc uses tables, W3Schools showed me the way, as you see below and in the style sheet.

### List Item Spacing
I use a lot of bulleted and numbered lists in my doc and like a little space between each item, so that's something I added to the style sheet.

### Color Scheme
Same as the original. Changing it may require changing the color of elements within (i.e text colors, black or white). Linear-gradient will be used if the browser supports it otherwise it will use the solid color specified.

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

### Google Analytics
There is a sample snippet in the _includes folder, but the statement to include it in the head section of the default html ***is commented out***. Update the snippet and then remove the comment after you get your GA account set up. That's all there is to it.

Tis all for now. Hope someone out there finds this Theme useful and lets me know. That would make my day.

Thanks for checking it out.

# Test Header1
paragraph text

Some Java code with highlighting. How do I get this to line up left/right with the rest of the content?

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

1. ordered list with break<br>
more text
2. list2
3. list3

* unordered text with break<br>
more text
* next bullet
    * four spaces to get nested bullet with break<br>
    and more text
    * and one more
    * last nested bullet
* last one

> blockquote text with break<br>more text
>
> second paragraph

## Test Header2


### Test Header3
text

#### Test Header4
text

##### Test Header5
text

End of Document
