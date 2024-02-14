## Modernist Theme for Github Pages by [TR Systems](https://TR-Systems.github.io/web/){:target="_blank"}
### Under Construction and Testing! (February 2024)
This theme started out by copying the design of the built-in [Github Pages Modernist Theme](https://github.com/pages-themes/modernist){:target="_blank"}.

If you're reading this on Github, click here to check it out on the web: [Modernist Theme by TR Systems](https://tr-systems.github.io/modernist/).

### Usage
Good for static display of system documentation and articles of interest on full screen browsers. Navigation is through the home page, thus the home page button on every page header. This page (README.md) is your home page, which will be built as index.html.

### Do Not Fork this Repo
This repo is defined as a template. When viewing TR-Systems/modernist on Github, click the green button in the upper right to ***Use this template***, ***Create new Repository*** and ***Include all Branches***.

### Use a Team/Pro Account
Even as a total newbie to Github, I recommend this low-cost option so you can use a custom domain name and publish from a private repo in a separate Team account (e.g TR-Systems), instead of publishing from a public repo on your personal account.

### Modifications
I only copied what was needed and then modified the style sheet, default html and config to get what you see here. I removed a lot of formatting and fluff that I didn't like from the overloaded style sheet (too many cooks in the kitchen).

### Editing and Publishing
The repo has two branches. Apply changes and new content to the top level "edit" branch, then pull them down into the "publish" branch for the automatic "pages build" process. There may be a better way but this works for me since I do all editing online. I will get around to using git on the desktop eventually.

### Make it Your Own
I have designed this site so ALL YOU NEED TO DO is **edit _config.yml, readme.md and about.md** to make it your own. And if you're like me and never really done this kind of thing before, open those files in the editor to see just how easy it is.

There are only a few other simple things you need to do in order to publish your web site, and that's where [Github Pages Help](https://docs.github.com/en/pages){:target="_blank"} comes in handy. All of Github is very well documented in their Help pages. Github for Dummies helped me out in the very beginning, too.

**_layouts/default.html** is used to build the header and footer and is substantially modified from the original. All content in the header and footer is supplied by variables in _config.yml. 

Two optional link buttons are provided in the upper right corner of the header. If not configured, they will not be displayed. The default html file controls that and the style sheet controls how the buttons are placed and squeezed together. Rather tricky. *So don't mess with the header section of the style sheet!* Actually, have at it. 

**_sass/modernist.scss** is the style sheet and since it was developed and modified over years in the public domain, it was a mess so I am still in the process of cleaning it up by first learning what everything does and then keeping only those mods and adding others to suit my style. So just grab it and go.

### Color Scheme
This page uses the color scheme from the original. Changing it may require changing the color of elements within (i.e text colors, black or white). Linear-gradient will be used if the browser supports it otherwise it will use the solid color specified.

| Background Colors | Color1 | Color2 |
| ----------------- | ------ | ------ |
| html: background: #6C7989; | <img width="48" src="images/color-6C7989.png"> | x |
| html: background: linear-gradient(#6C7989, #434B55) | <img width="48" src="images/color-6C7989.png"> | <img width="48" src="images/color-434B55.png"> |
| header: background: #C6EAFA; | <img width="48" src="images/color-C6EAFA.png"> | x |
| header: background: linear-gradient(#DDFBFC, #C6EAFA); | <img width="48" src="images/color-DDFBFC.png"> | <img width="48" src="images/color-C6EAFA.png"> |
| header: border-bottom:2px solid #B2D2E1; | <img width="48" src="images/color-B2D2E1.png"> | x |
| header:before: background:rgba(#000, 0.1); | BLACK | x |
| header:ul: background:#5198DF; | <img width="48" src="images/color-5198DF.png"> | x |
| header:ul: background: linear-gradient(#77B9FB, #3782CD); | <img width="48" src="images/color-77B9FB.png"> | <img width="48" src="images/color-3782CD.png"> |
| section: background:#FFFFFF; | WHITE | x |
| th: background-color: #3782CD; | <img width="48" src="images/color-3782CD.png"> | x |

### Google Analytics
There is a sample snippet in the _includes folder, but the statement to include it in the head section of the default html ***is commented out***. Update the snippet and then remove the comment after you get your GA account set up. That's all there is to it.

### Table Layout
I used the [CSS Reference](https://www.w3schools.com/cssref/index.php){:target="blank"} from W3Schools to learn how to be stylish. Very useful. And since my system doc uses tables, W3Schools showed me the way, and you will see how in the style sheet. For example, here is a list of the cars I owned from age 18 to 23.

| Year | Make | Model | Color | Years Owned | Notes |
| ---- | ---- | ----- | ----- | ----------- | ----- |
| 67 | Chevy | Impala Station Wagon | Baby Blue | 74-75 | Modified 327 with Edelbrock and Holley 4bbl<br>Wish I had this car now :) |
| 73 | Dodge | Charger | Turqoise w/<br>White Vinyl top | 75 | What was I thinking? |
| 72 | MGB | GT Coupe | BR Green | 75-76 | Wrecked it, not my fault |
| 67 | Chevy | Camaro | Brown/Black | 76-79 | For $750 cash after the wreck |

It gets rather boring and embarrassing too from there. And yes, there was and still is a mini-van in the list, absolutely, must have for home improviement project work and road trippin'.

Tis all for now, back soon. Hope someone out there finds this Theme useful and lets me know! That would make my day.

Thanks for checking it out.

# Test Header1
text here

1. text with break<br>
more text
2. text
3. text

* text with break<br>
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
text

### Test Header3
text

#### Test Header4
text

##### Test Header5
text

End of Document
