[HTML5 Template homepage](https://moosehead.studio/)

##Prerequisites

_Some of these are not required but we recommend it, it's how we are set up in house, it's tried and tested._

###[Brackets](http://brackets.io)
  * Plugins
    * git
    * scss-lint
    * markdown preview
    * custom work
    * editor config
    * swatcher
    * simple to do
  

###[Ruby](https://www.ruby-lang.org/en/downloads/)
To install ruby Gems once Ruby is install simply type
```gem install <GEMNAME>```
  * gems
    * Breakpoint
    * sass
    * scss_lint

###[PrePros](http://prepros.io)
Paid software, free to use.
or you can use [Koala](http://koalaapp.io) instead, which is 100% free

_You may also need Apple Command line tools if on Mac._
  **Mac OS X:** [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12) (or in terminal: `xcode-select --install`)
  
  **Windows:** [Visual Studio](https://www.visualstudio.com/products/visual-studio-community-vs) OR [Visaul Studio Code](https://code.visualstudio.com)
  
---

## Getting started

* [Usage](usage.md) — Overview of the projects structure.
* [FAQ](faq.md) — Frequently asked questions along with their answers.

## HTML5 Template core

* [HTML](html.md) — Guide to the default HTML.
* [CSS](css.md) — Guide to the default CSS.
* [JavaScript](js.md) — Guide to the default JavaScript.
* [SCSS](SCSS.md). -  Guide to the use of SCSS
* [BREAKPOINT](SCSS.md). - Guide to viewport-breakpoints

## Development

* [Extending and customizing HTML5 Template](extend.md) — Going further
  with the Template.
* [Everything else](misc.md). - Wondering what all the other files are?

##Breakdown.

Here we have the directory structure of the Moosehead.studio Boilerplate, in this you will see the directory structure of the template and how it may best suit your needs if you so choose to use it.

  > DIST
  
  >> CSS
  > * Compiled CSS files.
  > * Included source map; <i>'sourcemaps' are used by browser debuggers to show where the issue is linked in the relating SCSS files.</i>
    
  >> DOC
  > * The documentation for the bopilerplate.
  > * This is where you can get a better understanding of the templates features and what each individual feature and file does.
  
  >> FONTS
  > * This is where you house your custom fonts.
  > * Included is the material design fonts (icons)
  
  >> JS
  > * This is where your Custom scripts will be stored, read the included files descriptions to get a better understanding of how they are used
  >> VENDOR
  > * This is where you include your custom libraries, Jquery plugins etc.
  
> SASS
  > * This is where you put your SCSS files that will lated be compiled to CSS files (we store our SCSS libraries in here as well.
  >> MD-ICONS
  > * SASS files for material design icons.

```
.
├── CHANGELOG.html
├── CHANGELOG.md
├── LICENSE.txt
├── MooseheadStudioDirectoryTree.txt
├── README.html
├── README.md
├── dist
│   ├── LICENSE.txt
│   ├── browserconfig.xml
│   ├── css
│   │   ├── main.css
│   │   ├── main.css.map
│   │   ├── md-main.css
│   │   ├── md-main.css.map
│   │   ├── normalize.css
│   │   └── normalize.css.map
│   ├── doc
│   │   ├── TOC.md
│   │   ├── css.md
│   │   ├── extend.md
│   │   ├── faq.md
│   │   ├── html.md
│   │   ├── js.md
│   │   ├── misc.md
│   │   ├── scss.md
│   │   └── usage.md
│   ├── favicon.ico
│   ├── fonts
│   │   ├── MaterialIcons-Regular.eot
│   │   ├── MaterialIcons-Regular.ijmap
│   │   ├── MaterialIcons-Regular.svg
│   │   ├── MaterialIcons-Regular.ttf
│   │   ├── MaterialIcons-Regular.woff
│   │   ├── MaterialIcons-Regular.woff2
│   │   ├── README.md
│   │   └── codepoints
│   ├── humans.txt
│   ├── icon.png
│   ├── img
│   ├── index.html
│   ├── js
│   │   ├── main.js
│   │   ├── plugins.js
│   │   └── vendor
│   │       ├── jquery-3.3.1.min.js
│   │       └── modernizr-3.6.0.min.js
│   ├── robots.txt
│   ├── site.webmanifest
│   ├── tile-wide.png
│   └── tile.png
├── icon.png
├── modernizr-config.json
├── prepros-6.config
└── sass
    ├── MD-ICONS
    │   ├── _md-core.scss
    │   ├── _md-icons.scss
    │   ├── _md-mixins.scss
    │   ├── _md-variables.scss
    │   └── md-main.scss
    ├── _breakpoint.scss
    ├── _defaults.scss
    ├── _user-Styles.scss
    ├── breakpoint
    │   ├── _context.scss
    │   ├── _helpers.scss
    │   ├── _legacy-settings.scss
    │   ├── _no-query.scss
    │   ├── _parsers.scss
    │   ├── _respond-to.scss
    │   ├── _settings.scss
    │   └── parsers
    │       ├── _double.scss
    │       ├── _query.scss
    │       ├── _resolution.scss
    │       ├── _single.scss
    │       ├── _triple.scss
    │       ├── double
    │       │   ├── _default-pair.scss
    │       │   ├── _default.scss
    │       │   └── _double-string.scss
    │       ├── resolution
    │       │   └── _resolution.scss
    │       ├── single
    │       │   └── _default.scss
    │       └── triple
    │           └── _default.scss
    ├── main.scss
    └── normalize.scss

15 directories, 74 files

```
