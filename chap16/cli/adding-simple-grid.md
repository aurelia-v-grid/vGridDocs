####Adding grid to page

####app.js

* replace the app.js file content with this:

```javascript
// import our grid connector
// this is use to connect the grid to the datasource
import { GridConnector } from 'aurelia-v-grid';

// import our datasource, 
// this is the the class that we put our data into, it will comunicate with the grid through the grid connector
// this will also have some helper function to sort/add/filter etc
import { DataSource } from 'aurelia-v-grid';


export class App {
  constructor() {
    
    // simple dummy data
    this.personData = [];

    // loop to generate som data
    for(let i = 0; i< 1000; i++){
      this.personData.push({
        id:i,
        name:'person' + i,
        country:'country' + i,
        bool: i % 3 === 0 ? true: false
      })
    }

    // create datasource (you could just inject this from somewhere else)
    this.personDatasource = new DataSource();
    
    //create grid connector
    this.gridConnector = new GridConnector(this.personDatasource);
    
    // set data to the datasource, you dont need to set data now, you can do it later...
    this.personDatasource.setArray(this.personData);
  }
}
```

####app.html



* replace the app.js file content with this:

```html
<template>

  <!--Our grid element-->
  <!--please notice the v-grid-connector attibute, this is the same as the one in the app.js-->

  <v-grid 
    v-grid-connector.bind="gridConnector"   
    style="height:400px;width:400px">
    
    <!--Grid columns with just name of the attibute we want it to display-->

    <v-grid-col col-field="id"></v-grid-col>
    <v-grid-col col-field="country"></v-grid-col>
    <v-grid-col col-field="name"></v-grid-col>
    <v-grid-col col-field="bool"></v-grid-col>

  </v-grid>

</template>
```