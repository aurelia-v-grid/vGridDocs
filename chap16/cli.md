#Getting started

We will now generate a simple ES6 skeleton to work with Aurelia-CLI and add the grid as a plugin

If you have not installed the CLI then please do so like this:
`npm install aurelia-cli -g`

Aurelia-CLI:
> For more info regarding the CLI install etc, see the docs : http://aurelia.io/hub.html#/doc/article/aurelia/framework/latest/the-aurelia-cli



---

####Generating the project

![](/assets/01-new cli project.png)


1. Lets now generate a new project, open the cmd/terminal and under your documents and type 
>`au new`

2. Lets now write the name of our app (see below) and hit enter
> `vgridSample`

3. On the next questions just choose the default ES6 skeleton, yes to create and install dependencies (installing dependencies can take a while...)

####Adding the plugin

* To install the plugin you need to enter the new project folder and run this:
> `npm install git://github.com/vegarringdal/vGrid.git#dev-rebuild --save`

* Now open this file(see below) in you project folder
> `vGridSample\aurelia_project\aurelia.json`

* Add this under `bundles/vendorbundle/dependencies` in the json file

```json
{
    "name": "aurelia-v-grid",
    "path": "../node_modules/aurelia-v-grid/dist/amd",
    "main": "index",
    "resources": [
        "**/*.{css,html,js}",
        "grid/v-grid-row-repeat.js",
        "grid/v-grid-group-row.js ",
        "grid/v-grid-group-element.js",
        "grid/v-grid-loadingscreen.js",
        "grid/v-grid-contextmenu.js",
        "grid/v-grid-footer.js",
        "grid/v-grid-col.js",
        "grid/attributes/v-drag-drop-col.js",
        "grid/attributes/v-filter.js",
        "grid/attributes/v-filter-observer.js",
        "grid/attributes/v-data-handler.js",
        "grid/attributes/v-image.js",
        "grid/attributes/v-changed.js",
        "grid/attributes/v-menu.js",
        "grid/attributes/v-resize-col.js",
        "grid/attributes/v-sort.js",
        "grid/attributes/v-selection.js",
        "grid/styles/cellsAndLabels.css",
        "grid/styles/contextmenu.css",
        "grid/styles/grouping.css",
        "grid/styles/dragAndResize.css",
        "grid/styles/icons.css",
        "grid/styles/loader.css",
        "grid/styles/main-element-tags.css",
        "grid/styles/main-elements.css"
    ]
}
```

* Under `loader/plugins/text/stub` in the json file, you need to set stub to false.

```json
"loader": {
    "type": "require",
    "configTarget": "vendor-bundle.js",
    "includeBundleMetadataInConfig": "auto",
    "plugins": [{
      "name": "text",
      "extensions": [
        ".html",
        ".css"
      ],
      "stub": false
    }]
  },
```
*  Now open the `src/main.js` and add "addPlugin()" 

```javascript

import environment from './environment';

export function configure(aurelia) {
  aurelia.use
    .standardConfiguration()
    .feature('resources')
    .plugin('aurelia-v-grid')

  if (environment.debug) {
    aurelia.use.developmentLogging();
  }

  if (environment.testing) {
    aurelia.use.plugin('aurelia-testing');
  }

  aurelia.start().then(() => aurelia.setRoot());
}
```

####You are done!

* To run app type ```au run --watch``` and open the `hhttp://localhost:9001` in the browser
* You should see "hello world" on you screen, please open console and check that you have no errors


