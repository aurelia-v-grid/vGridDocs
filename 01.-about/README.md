# About \(readme first\)

{% hint style="info" %}
You need to read entire about section before you try and use it!!!
{% endhint %}

{% hint style="info" %}
Read chapter "Install" for how to get it installed \(bottom in right menu\)
{% endhint %}

To work use and connect to the grid you will need to use built in data source and grid connector. If you also need selection in the grid, you will also need to import this.

Datasource handles all the filtering/sorting of the data, data needs to be object array. Look in sample code below how to get started, there is a own article on all the methods in the datasource.

Grid connector is the link between the GUI part and datasource, this is the part that gets binded in the html.

> _TODO... explain more, I need to add a step by step guide for new people_

```text
import { GridConnector } from 'aurelia-v-grid';
import { DataSource } from 'aurelia-v-grid';
import { Selection } from 'aurelia-v-grid';


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

    // create datasource (you could just inject this from somewhere else)
    this.ds = new DataSource(new Selection('multiple'));

    //create grid connector
    this.gridConnector = new GridConnector(this.ds);

    // set data to the datasource, you dont need to set data now, you can do it later...
    this.ds.setArray(this.collection);
  }


}
```

You should add valueConverter to keep number as number, and boolean as boolean, else the values will be converted to string by aurelia binding system, unless you use some custom datasource with the grid

```markup
<template>
      <v-grid 
        v-multi-select="true" 
        v-grid-connector.bind="gridConnector" 
        v-row-height="25" 
        v-header-height="50" 
        v-panel-height="25"
        v-footer-height="25" 
        style="height:400px;width:400px">
        <v-grid-col col-field="bool | booleanConverter"></v-grid-col>
        <v-grid-col col-filter-menu="filter:country"col-field="country"></v-grid-col>
        <v-grid-col col-field="name"></v-grid-col>
        <v-grid-col col-field="number  | numberConverter"></v-grid-col>
      </v-grid>
</template>
```

Sample boolean and number value converters you can start with.

```javascript
export class NumberFormatterValueConverter {
  public toView(value: any) {
    if (value) {
      return value;
    } else {
      return value;
    }
  }

  public fromView(value: any) {
    if (value) {
      let check = value * 1;
      if (isNaN(check)) {
        return value;
      } else {
        return value * 1;
      }

    } else {
      return value;
    }
  }
}

// tslint:disable-next-line:max-classes-per-file
export class BooleanFormatterValueConverter {
  public toView(value: any) {
    if (value) {
      return value;
    } else {
      return value;
    }
  }

  public fromView(value: any) {

    if (typeof value === 'string') {
      value = value.toLowerCase();
      switch (value) {
        case 'true':
          value = true;
          break;
        case 'false':
          value = true;
          break;
        default:
          value = false;
      }
    }


    return value;
  }
}


// tslint:disable-next-line:max-classes-per-file
export class DisplayFormatNumberValueConverter {
  public toView(value: any) {
    if (value) {
      return '$' + value;
    } else {
      return value;
    }
  }

  public fromView(value: any) {
    if (value) {
      let check = value * 1;
      if (isNaN(check)) {
        return value;
      } else {
        return value * 1;
      }

    } else {
      return value;
    }
  }
}
```

