# Aurelia-CLI \(asp-core\)

_-Tested with esnext default :**not tested**_

* Run: `npm install aurelia-v-grid --save`
* In `main.js` add `.plugin('aurelia-v-grid')`
* Add to aurelia\_project/aurelia.json

  ```text
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
            "grid/attributes/v-menu.js",
            "grid/attributes/v-resize-col.js",
            "grid/attributes/v-changed.js",
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
    },
  ```

* set stub to false in the loader/plugins in aurelia\_project/aurelia.json  
  \`\`\`  
  "loader": {

  ```text
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
  ```

  },\`\`\`

