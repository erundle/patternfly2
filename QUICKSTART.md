# Using [PatternFly](https://www.patternfly.org) - Quick Start Guide

This reference implementation of PatternFly is based on [Bootstrap v3](http://getbootstrap.com/).  Think of PatternFly as a "skinned" version of Bootstrap with additional components and customizations. PatternFly is meant to be used as a replacement for Bootstrap so please don't include the PatternFly CSS and Bootstrap CSS in your project. 

### What's included

Within the download you'll find the following directories and files, logically grouping common assets and providing both compiled and minified variations. You'll see something like this:

```
patternfly/
├── components/
│   ├── 3rd Party Repos. May need to pull in additional JS includes based on Patternfly Usage (No additional CSS includes needed)
├── dist/
│   ├── css/
│   │   │── patternfly.min.css (* Need to include)
│   │   │── patternnfly-additions.min.css (* Need to include)
│   └── fonts/
│   │   │── Font and icon libraries (Already included via CSS - Nothing to do here)
│   └── img/
│   │   │── Branding Materials and Loading Indicators
│   └── js/
│   │   │── patternfly.min.js (May need to include if you are using Patternfly jQuery Sidebar, Popovers or Datatables)  
├── less/
│   ├── Variables, Mixin, and Component LESS files. May need to include if you want to customize the already built CSS
└── test-src/
    ├── Example Code Src Files
```

We provide compiled CSS and JS (`patternfly.*`), as well as compiled and minified CSS and JS (`pattternfly.min.*`). CSS [source maps](https://developer.chrome.com/devtools/docs/css-preprocessors) (`patternfly.*.map`) are available for use with certain browsers' developer tools. Fonts from OpenSans, FontAwesome, Patternfly Icons are included, as well as numerous other 3rd party JS components and libraries.

## Using Patternfly In Your Application

1. Ensure you have installed the following utilities:
    - [Git](http://git-scm.com/downloads): a free and open source distributed version control system.
        - Unfamiliar with Git? I recommend using [GitHub for Windows](https://windows.github.com/) or [GitHub for Mac](https://mac.github.com/).
    - [Node.js](http://nodejs.org/download/): a software platform that is used to build server-side applications.
    - [Grunt](http://gruntjs.com/getting-started): a JavaScript task runner.

            $ sudo npm install -g grunt-cli

    - [Bower](http://bower.io/#installing-bower): a package manager for the web.

2. Add Patternfly as a dependency for your project and you'll receive all the libraries you'll need:

        $ bower install patternfly --save

    For full install options see the [README](README.md)

3. Add the follwing CSS includes to your HTML file(s), adjusting path where needed:

        <!-- Patternfly Styles -->
        <!-- Note: No other CSS files are needed regardless of what other JS packages located in patternfly/components that you decide to pull in -->
        <link rel="stylesheet" href="bower_components/patternfly/dist/patternfly.min.css" />
        <link rel="stylesheet" href="bower_components/patternfly/dist/patternfly-additions.min.css" />

4. Add the following script includes to your HTML file(s), adjusting where necessary to pull in only what you need:

        <!-- jQuery -->
        <script src="bower_components/patternfly/components/jquery/dist/jquery.js"></script>

        <!-- Bootstrap JS -->
        <script src="bower_components/patternfly/components/bootstrap/dist/js/bootstrap.js"></script>

        <!-- Patternfly Custom Componets -  Sidebar, Popovers and Datatables Customizations -->
        <script src="bower_components/patternfly/dist/js/patternfly.js"></script>

        <!-- C3, D3 - Charting Libraries -->
        <script src="bower_components/patternfly/components/c3/c3.min.js"></script>
        <script src="bower_components/patternfly/components/d3/d3.min.js"></script>

        <!-- Datatables, jQuery Grid Component -->
        <!-- Note: jquery.dataTables.js must occur in the html source before patternfly*.js.-->
        <script src="bower_components/patternfly/components/datatables/media/js/jquery.dataTables.js"></script>
        <script src="bower_components/patternfly/components/datatables-colvis/js/dataTables.colVis.js"></script>
        <script src="bower_components/patternfly/components/datatables-colreorder/js/dataTables.colReorder.js"></script>

        <!-- Bootstrap Date Picker -->
        <script src="bower_components/patternfly/components/bootstrap-datepicker/dist/js/bootstrap-datepicker.min.js"></script>

        <!-- Bootstrap Combobox -->
        <script src="bower_components/patternfly/components/bootstrap-combobox/js/bootstrap-combobox.js"></script>

        <!-- Bootstrap Select -->
        <script src="bower_components/patternfly/components/bootstrap-select/dist/js/bootstrap-select.min.js"></script>

        <!-- Bootstrap Tree View -->
        <script src="bower_components/patternfly/components/bootstrap-treeview/dist/bootstrap-treeview.min.js"></script>

        <!-- Google Code Prettify - Syntax highlighting of code snippets -->
        <script src="bower_components/patternfly/components/google-code-prettify/bin/prettify.min.js"></script>

        <!-- MatchHeight - Used to make sure dashboard cards are the same height -->
        <script src="bower_components/patternfly/components/matchHeight/jquery.matchHeight.js"></script>

        <!-- Angular Application? You May Want to Consider Pulling Angular-Patternfly And Angular-UI Bootstrap instead of bootstrap.js -->
        <!-- See https://github.com/patternfly/angular-patternfly for more information -->

5. Enjoy!!!




