#How to install
This chapter shows how to add/install the grid to your own project.

---
###JSPM:
 *-Tested with esnext skeleton:**working***
* Run: ````jspm install aurelia-v-grid=github:aurelia-ui-toolkits/aurelia-v-grid```
* In ```main.js``` add ```.plugin('aurelia-v-grid')```

---
###Aurelia-CLI (not asp.core)
*-Tested with esnext default :**working***
* Run: ```npm install git://github.com/aurelia-ui-toolkits/aurelia-v-grid.git --save```
* In ```main.js``` add ```.plugin('aurelia-v-grid')```
* Add to aurelia_project/aurelia.json
```
  {
    "name": "aurelia-v-grid",
    "path": "../node_modules/aurelia-v-grid/dist/amd",
    "main": "index"
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


---

###Aurelia-CLI (asp-core)
*-Tested with esnext default :**working***
* Run: ```npm install git://github.com/aurelia-ui-toolkits/aurelia-v-grid.git --save```
* In ```main.js``` add ```.plugin('aurelia-v-grid')```
* Add to aurelia_project/aurelia.json
```
  
  {
      "name": "aurelia-v-grid",
      "path": "../node_modules/aurelia-v-grid/dist/amd",
      "main": "index",
      "resources": [
        "vGrid/v-grid-element-footer-pager.js",
        "vGrid/v-grid-element-row-repeat.js",
        "vGrid/v-grid-element-col-config.js",
        "vGrid/v-grid.js",
        "vGrid/v-grid-attributes-sort.js",
        "vGrid/v-grid-attributes-filter.js",
        "vGrid/v-grid-attributes-selection.js",
        "vGrid/v-grid-attributes-image.js",
        "vGrid/v-grid-attributes-key-move.js",
        "vGrid/v-grid-attributes-contextmenu.js",
        "vGrid/v-grid-attributes-observe-field.js",
        "vGrid/v-grid-attributes-dragDropCol.js",
        "vGrid/v-grid-attributes-resize-col.js",
        "vGrid/v-grid-element-footer-pager.html",
        "vGrid/v-grid.html",
        "vGrid/styles/v-grid.css",
        "vGrid/styles/v-grid-draggable.css",
        "vGrid/styles/v-grid-contextmenu.css",
        "vGrid/styles/v-grid-loader.css",
        "vGrid/styles/v-grid-pager.css",
        "vGrid/styles/v-grid-sorticon.css",
        "vGrid/styles/v-grid-optional.css"
      ]
    },
  
  ```

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



---



###Webpack
*-Tested with esnext skeleton:**working***
* Run: ```npm install git://github.com/aurelia-ui-toolkits/aurelia-v-grid.git --save```
* In ```main.js``` add ```.plugin('aurelia-v-grid')```

---

###Without installing
*-Tested with aurelia-CLI:**working**, and prb all other esnext except typescript*
* If you dont want to install it, and just want to copy and run you can do this:
* Copy "vGrid" folder here over to "src" in skeleton from here: [link](https://github.com/aurelia-ui-toolkits/aurelia-v-grid/tree/master/src)
* In ```main.js``` add ```.plugin('vGrid/plugin')```

