# Aurelia-CLI (not asp.core)

*-Tested with esnext default :**tested***
* During development Im testing a remote datasource, so you also need o add ""aurelia-fetch-client" to project, will remove later
* Run: ```npm install git://github.com/vegarringdal/vGrid.git#dev-rebuild --save```
* In ```main.js``` add ```.plugin('aurelia-v-grid')```
* Add to aurelia_project/aurelia.json
```
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
            "grid/attributes/v-image.js",
            "grid/attributes/v-onchanged.js",
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
        }```

---
* set stub to false in the loader/plugins in aurelia_project/aurelia.json
```
  "loader": {
      "type": "require",
      "configTarget": "vendor-bundle.js",
      "includeBundleMetadataInConfig": "auto",
      "plugins": [
        {
          "name": "text",
          "extensions": [
            ".html",
            ".css"
          ],
          "stub": false <---------------------THIS ONE!!!!
        }
      ]
    },```