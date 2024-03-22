---
title: Get Started Today!
toc: toc-getstarted.html
print: print-button.html
---

Step by step process for beginners, new to GitHub. It's easy to create an account and get started today.

### Use a Team/Pro Account
Even as a total newbie to GitHub, I recommend this low-cost option so you can use a custom domain name and publish from a private repo in a separate Team account instead of publishing from a public repo on your personal account.

### Editing and Publishing
It's important that you understand the process. The repo has two branches. With this design, you will be applying all changes and new content to the top level **edit** branch. When everything looks good, you will then **pull** those changes into the **publish** branch for the automatic **Pages Build and Deploy** action that will be executed after each commit to the that branch.

Steps 1 and 2 will create the repository for your new website and then publish the site without making any changes, to simply insure that the process works for you, before you start making it your own.

### Step 1: Create the Repository

1. Login to GitHub and open [TR-Systems/modernist](https://github.com/tr-systems/modernist){:target="_blank"}
2. Click the button in the upper right to <span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Use this template</span> and select create new repository.
3. **Create a New Repository** appears. **Owner** will default to your GitHub userid. Switch to your Team account if using one. Give your repo a **short web-friendly name** like "web" or "mycoolthing" since the repo name is the top level path in the url to your site. **DO NOT include all branches.** If using a personal account, you must create a public repo, and only one of your public repos can have a website. This restriction does not apply for Team accounts.
4. Click <span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Create repository</span>
5. The repo will be copied and created. You are looking at it now.
6. Create the **publish** branch by clicking on the **edit** branch button, then **type "publish"** and then **click the line** that says **create branch publish from edit**, as shown here by clicking this button:

<div class="dropdown">
<button type="image" onclick="editButtonClick()" style="margin-left:24px; margin-bottom:6px; padding:0;">
<img src="images/edit.png" style="height:20px; width:80px;">
</button>
<div id="editContent" class="drop-content" style="position:relative; margin-left:24px; background-color:aliceblue; box-shadow:none; padding:0;">
<img src="images/createbranch.png">
</div>
</div>

### Step 2: Publish the Site

1. You now have the publish branch open.
2. Click the repo  <i class="material-icons" style="font-size:14px;">settings</i>**Settings** button.
3. In the nav bar on the left, click **Pages**
4. **Build and deployment** appears. Select **Deploy from branch**, **publish** /root. Click **Save**.
5. GitHub will kick off the Pages Build and Deploy action
6. Click on **Actions** to watch that process run
7. Go back to **Settings/Pages** and click the link to visit your site

Voila, web sites made easy! Ha! Your job has just begun. Have fun!

---

## Step 3: Make it Your Own
All you need to do is edit a few files to make it your own for starters. And if you're like me and never really done this kind of thing before, open those files in the editor to see just how easy it is to use GitHub markdown formatting for your content. [Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github){:target="_blank"} may cone in handy, too. All of GitHub is very well documented in their Help pages but it can be overwhelming and so much of it doesn't apply for the simple thing we're doing with here.

For me, the best way to learn has been by example, so that's why I have loaded up these pages with everything I could think of, including some fancy HTML stuff, like that button and those green boxes above.

So you may want to keep this page and the design page as references and also add them to the exclude statement in the config file so they aren't included in the build process for your site.

### Step 4: Edit config.yml
Make sure you are editing in the edit branch! This is where you will fill in all of personal header and footer information.

**Important:** Update the **url** variable to the url of your new website.

**Note** that all header and footer content variables other than your site **title** are OPTIONAL.

**TIP:** Keep your site **title** relatively short for best viewing on a phone or tablet, especially if you are going to use all three of the link buttons in the header. The goal is to keep the title and link buttons on the same line when viewing on a phone.

You may now want to add **design.md** and **getstarted.md** to the **exclude** variable and remove the links to those pages from the **link3** variable and from the **site-menu.html and toc-homepage.html** files.

### Step 5: Edit index.md
This is your home page. Make it your own. I have configured it so the **toc** and **site menu** buttons both have the same links, which is not normal, simply illustrative of what you can do. Both are optional.

### Step 6: Edit about.md
Tell the world what this is all about.

### Step 7: Publish Your Changes
This process will create a **pull request** to apply your changes to the files in the publish branch. There are other ways to initiate the pull request but they all end up at the same place.

1. Switch to the **publish** branch by clicking on this button again:
<img src="images/edit.png" style="height:20px; width:80px;"> If you have edited all three files, you will see that it is <span style="color:#069;text-decoration:underline;">3 commits behind</span> the edit branch. **Click on that link**.
2. **Comparing Changes** appears. Scroll down to view the changes.<br>
Click <span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Create pull request</span>
3. **Open a Pull Request** appears, where you can enter a title (required), optional description and view the changes again.<br>
Click <span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Create pull request</span> again
4. GitHub checks to see if there are any conflicts between the two branches. There won't be as long as you NEVER edit and commit any changes directly to the publish branch. Click <span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Merge pull request</span>
5. Click <span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Confirm Merge</span>
6. Click Actions to watch **Pages Build and Deploy** run.

And that's it, in a nutshell. Make changes to the edit branch and pull them down to publish.

---

### Technical Reference
#### <span style="color:#069">_layouts/default.html</span>
Defines the HTML structure of your pages and is where the values of the config variables are placed on the page.

#### <span style="color:#069">assets/css/style.scss</span>
Defines how all content appears on your pages and is referenced in the <head> section of **default.html**.

#### <span style="color:#069">images</span>
Cut and crop your image files way down in size and resolution before uploading to this folder and using them in your pages. You can fine-tune the size of an image on a page using width, height or percent settings when you reference it. There is much more to this topic than I can possibly share with you here. Just don't upload full resolution pics from your camera.

#### <span style="color:#069">_includes</span>
This is where you will define your **site menu** for all pages and a **table of contents** for any page that warrants, which are referenced in **default.html**. The **site menu** is called out in the **config** file using the **menu** variable. A **toc** is called out in the front matter of the page using the **toc** variable.

#### <span style="color:#069">print-button.html</span>
If you want the print button to appear in the header, call it out in the front matter of your page using the **print** variable.

#### <span style="color:#069">button-script.html</span>
This is the script that displays the dropdown list for the site menu and toc buttons when clicked and is placed in the <head> section of **default.html**. Currently, it will only hide the toc content when you click elsewhere on the page. So for now, the only way to hide the site menu is to click on it again. This is a work in progress and a major change in the script and methods being used is required. Still learning.

---

#### Google Analytics
Google Analytics is configured for the GA stream "**tr-systems.github.io/modernist/**" by using an **if** statement in **_layouts/default.html** that you will need to update after you get your own GA account and stream set up, along with the GA code snippet in the **_includes** folder, should you so desire. Yyou can leave it all in place for now. The GA code snippet won't be included in your pages.

---

## Develop and Test on Windows
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

## Develop and Test on Ras Pi
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

End of Document
