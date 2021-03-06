# Culture Coding website

## Use cases

### 1. Traveling to somewhere or waiting something.

* Motivation to use: Fight against boredom
* Device: Mobile, sometimes: tablet

### 2. Surf internet and follow links (e.g. from another website or SoMe)

* Motivation to use: Find out if CC is something interesting, read more on CC, exampine
* Device: Desktop or tablet; sometimes mobile

### 3. Socialize

* Motivation to use: Do something interesting with friends or share something interesting for them
* Device: any
* Notes: Sharing links to SoMe

### 3. Introduce idea to someone (e.g. in cafe/restauran, or in event)

* Motivation to use: Keypoints what is CC, show & use examples
* Device: Mobile, sometimes: tablet or laptop

### 4. Use code to create value e.g. in a creative workshops

* Motivation to use: varying external motivations, e.g. find a tool to generate ideas or think out of the box
* Device: Desktop, printer


## Ideas and constraints

### General

* Mobile first design. In many common use cases the site is used by a mobile device or by tablet.
* Twitter handle?

### Landing page structure

* Title (Cultere Code and Culture Coding are both possible, former is prefered.)
* Short motto under the title
* Synopsis (~three sentences, only little text, possibly some icons or images)
* Featuring code (jotta sivu näyttää erillaiselta)/News/Events. Something that changes and give user a motivation to return.
* Code listing & once there are more than 20 codes nice search. In the beginning there need not be many codes (mayby 5-10). Quality over quantity.

### Code pages

* Easy to read with any device
* Easy to share

### Images

* Frames?
* Symbolic picture? Also photos?


# Technical instructions

## How it works

- Website is build on [Jekyll](http://jekyllrb.com/). Jekyll is Blog-aware engine that generates plain html-sites. I.e. there is no server-side logic for rendering pages to user - just static files. Even if the "compiled" Jekyll sites consist of static files, there's quite a lot of logic for the site generation. You can have "master pages" or "pages templates", and you can have reusable components. The actual content pages are either [Markdown markup language](https://guides.github.com/features/mastering-markdown/) (with [GitHub flavour](https://help.github.com/articles/github-flavored-markdown/)) or plain HTML (or both because in Markdown you can use HTML). In addition to can have arbitraty metadata for a page.
- Responsive layout is build by using [Bootstrap](http://getbootstrap.com/css/#grid-example-wrapping)
- CSS is generated by using [LESS](http://lesscss.org/) (mainly because Bootstrap uses LESS)
- CSS and JavaScript minification utilizes [Grunt](http://gruntjs.com/) task runner.

## Installing development enviroment

In order to produce content you need to install:

1. [Git](https://git-scm.com/). Instead of installing Git from that site you may install a decent GUI (by installing one you get also git commandline utility). There are many GUIs to git, including the simply awful default GUI of Git. In this case GitHub's own is probably good enough. Install: [GitHub for Mac](https://mac.github.com/) or [GitHub for Windows](https://windows.github.com/). (I have not used these myself, but it seems to be relatively easy to use. I use Git commandline utility because it is faster and more flexible --- after youhave learned how to use it.)
3. [Ruby v. 2.0 or newer](http://ruby-lang.com). Notice that the default installation of Ruby is conservatively v. 1.9.x. GitHub pages recommends to use Ruby 2.0+. Depending on the way you've installed Ruby, you may need to install Ruby Development Tools; e.g. I installed Ruby to Linux Mint by using apt-get, and I needed to install dev tools in addition. If you use an installation wizard, you probaly can choose to install dev tools.
4. [Jekyll](http://jekyllrb.com/). After you have installed Ruby, install Jekyll by runing in shell/command prompt: ```gem install jekyll```. (If you get error you probably don't have Ruby development tools installed for the correct version of ruby. Google the error, you probably find out the way to installe them to your OS.)

That all.

Next just get the source code from GitHub and run ```jekyll serve``` in the folder the source code are located. Once Jekyll development server is up and running, open browser and go to [http://localhost:4000](http://localhost:4000)

---

If you want to modify styles or write JavaScript logic you have to install also:

1. [NodeJS](https://nodejs.org/). Currently, it is used for Css and JavaScript minification and css compilation (LESS). Compliled files are stored to Git, and thus, if you only produce content and need not tweak styles or JavaScript you don't need Node.js.
2. Grunt command line utility. After you have installed NodeJS but run in shell/command prompt: ```npm install grunt-cli --global```

To recompile, bundle and minify CSS and JavaScript run: ```grunt``` in the root folder of the repository folder.

## Downloading the source code

If you installed GitHub for your OS, well --- read the getting strated tutorial: [GitHub for Mac help page](https://mac.github.com/help.html) and [GitHub for Windows help page](https://windows.github.com/help.html).

If you chose to use git bash, save you nerves and create first ssh-key for git. GitHub have [pretty good instructions](https://help.github.com/articles/generating-ssh-keys/).

After you have configured ssh-key, run in the root folder of your git project (in window I use c:\git and in Linux ~\git\. The root folder can be anything you like. However, in Windows you want that it is very short and close to root, because in some (rare) cases 255 path lenght limitation may cause problems.):
```
cd [your root folder for git projects]
git clone git@github.com:CultureCoding/CultureCoding.github.io.git
```

TODO add link to good git bash tutorial.

## Modifying and adding pages

- You can add raw html-pages or use markdown-wikisyntax.
- There are two kind of pages in Jekyll: post and pages. The difference is that post needs to have publish page encoded in the title, pages don't. In addition there are quite a lot of Open source plugins for listing post and not that many for listing pages.
- Jekyll have nice collection of simple buildin functions e.f. for page listings and dynamic linking. See [Jekyll documentation](http://jekyllrb.com/)
- You can create reusable components (e.g. navis or banners) and page templates easily. See [templates in Jekyll documentation](http://jekyllrb.com/)
- You can write more complex logic by Ruby. It relatively easy, but you need to know basic of Ruby and understand how Jekyll tags and templates works.

