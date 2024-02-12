## Modernist Theme for Github Pages by [TR Systems](https://TR-Systems.github.io/web/){:target="_blank"}
### Under Construction!
This theme started out by copying the design of the built-in [Github Pages Modernist Theme](https://github.com/pages-themes/modernist){:target="_blank"}.
### Usage
Good for static display of system documentation and articles of interest on full screen browsers. Navigation is through the home page, thus the home page button on every page header. This page (README.md) is your home page, which will be built as index.html.
### Modifications
I only copied what was needed and then modified the style sheet, default html and config to get what you see here. I also removed a lot of fluff that isn't needed from the overloaded style sheet (too many cooks in the kitchen), such as all of the text and box shadows, which only makes text blurry. Shadows are good only for really LARGE CAP fonts and the box shadows were defined with only 1 or 2px so hardly even visible. Those are all gone, about a dozen specs in all.

I used the reference available from W3Schools to learn all about style sheets and how to test things. Very useful. And since my system doc uses tables, W3Schools showed me the way, and you will see how in the style sheet.

| Year | Make | Model | Color | Years Owned | Notes |
| ---- | ---- | ----- | ----- | ----------- | ----- |
| 67 | Chevy | Impala Station Wagon | Baby Blue | 74-75 | 327 with Edlebrock and Holley 4bbl |
| 73 | Dodge | Charger | Turqoise w/<br>White Vinyl top | 75 | Too much |
| 72 | MGB | GT Coupe | BR Green | 75-76 | Wrecked it, not my fault |
| 67 | Chevy | Camaro | Brown/Black | 76-79 | $750 cash |

Best stop there before I get into the mini-van years!


### Editing and Publishing
The repo has two branches. Apply all changes and new content to the top level "edit" branch, then pull them down into the "publish" branch for the automatic "pages build" process. I'm all new at github so there might be a better way to manage changes and publishing but this works for me.

The default html is used to build the header and footer and is substantially modified from the original. All content in the header and footer is supplied by variables in _config.yml with the exception of the Home Page button. Two additional link buttons are provided in the upper right corner of the header. If not configured, they will not be displayed. The default html file controls that and the style sheet controls how they are built and squeezed together. Rather tricky.

Experienced users know all that and can take it from here. Beginners may want to check back or send me a message.

### Google Analytics
There is a sample google analytics snippet in the _includes folder, but the statement to include it in the head section of the default html ***is commented out*** so you can come back after you get your site set up and put it back in, after you have updated the snippet. That's all there is to it.

