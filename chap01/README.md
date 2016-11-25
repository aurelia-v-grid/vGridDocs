#About the grid




Read chapter 10 on how to install


*TODO....*
Say something how its all connected, datasource, gridconnector

*TODO....*
show sample on how to get someting displayed

```
import { autoinject } from 'aurelia-framework';
import { GridConnector } from 'aurelia-v-grid';
import { DataSource } from 'aurelia-v-grid';
import { Selection } from 'aurelia-v-grid';


@autoinject()
export class Welcome {

  public ds: DataSource;
  public gridConnector: GridConnector;
  private myCollection: any;
  
  constructor() {
    
    //dummy data
    this.collection = [{
      name:'Vegar',
      number: 5425.25,
      country:'Norway',
      hired:true
      },{
      name:'Lars',
      number: 545.45,
      country:'Sweden',
      hired:false
    }]
    
    // create datasource
    this.ds = new DataSource(new Selection('multiple'));
    
    //create grid connector
    this.gridConnector = new GridConnector(this.ds);
    
    // set data to the datasource
    this.ds.setArray(this.myCollection);
  }


}
```


```
<template>
      <v-grid 
        v-multi-select="true" 
        v-grid-connector.bind="gridConnector" 
        v-row-height="25" 
        v-header-height="50" 
        v-panel-height="25"
        v-footer-height="25" 
        style="height:400px;width:400px">
        <v-grid-col col-field="bool | booleanFormatter"></v-grid-col>
        <v-grid-col col-filter-menu="filter:"country"col-field="country"></v-grid-col>
        <v-grid-col col-field="name"></v-grid-col>
        <v-grid-col col-field="number"></v-grid-col>
      </v-grid>
</template>

```


















