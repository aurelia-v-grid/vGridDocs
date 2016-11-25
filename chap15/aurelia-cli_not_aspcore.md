# Aurelia-CLI (not asp.core)

*-Tested with esnext default :**not tested***
* Run: ```npm install git://github.com/vegarringdal/vGrid.git --save```
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