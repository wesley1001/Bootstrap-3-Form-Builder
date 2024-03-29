#Bootstrap Form Builder

Original Source with bootstrap v2:
[Go to original repository](https://github.com/minikomi/Bootstrap-Form-Builder) by [minikomi](https://github.com/minikomi)

##What's this?

A Drag-and-drop form builder for [twitter bootstrap](http://twitter.github.com/bootstrap/). 

Currently using `v. 3.0.0`

##Where can I see it in action?

It's hosted on github pages [here](http://minikomi.github.io/Bootstrap-Form-Builder/).

###Notes

* For development & debugging change the data-main for the require script tag in `index.html` 
  to point at `assets/js/main.js`. (Look just before the closing `<body>` tag!)

* Once done, change it back to  build for production using the `build.js` script in the `assets/js/lib`
  folder and [r.js](https://github.com/jrburke/r.js/). Then revert to `assets/js/main-built.js`

* The full command is `r.js -o assets/js/lib/build.js` which should be run from the base directory.

### Adding new form elements

* In the [js/data/yaml folder](https://github.com/minikomi/Bootstrap-Form-Builder/tree/gh-pages/assets/js/data/yaml) are yaml files, each of which corresponds to a tab in the form builder.
* If you just want to add a new element you need to:
  - describe it in one of these files
  - parse the yaml to json using parse.rb in the same folder
  - create a corresponding template in the [templates/snippet directory](https://github.com/minikomi/Bootstrap-Form-Builder/tree/gh-pages/assets/js/templates/snippet)
  - add the template to [snippet-templates.js](https://github.com/minikomi/Bootstrap-Form-Builder/blob/gh-pages/assets/js/templates/snippet/snippet-templates.js)
* If you want to add a new tab, you'll also need to adjust the [app.js file](https://github.com/minikomi/Bootstrap-Form-Builder/blob/gh-pages/assets/js/app.js) to make sure the tab is loaded.

Don't forget to switch to main.js rather than main-built.js, or the changes you make before compiling with require.js won't show up!
