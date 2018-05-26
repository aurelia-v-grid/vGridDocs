# v-columns

Binding columns with array, instead of using html

```text
v-columns.bind="myColumns"
```

App.js

```text
import { GridConnector } from 'aurelia-v-grid';
import { DataSource } from 'aurelia-v-grid';
import { Selection } from 'aurelia-v-grid';

export class App{

    constructor(){

        this.data =[
            {name:"Per"},
            {name:"Per"},
            {name:"Per"}]

        this.myColumns =[
            {colField:"name"}]    

        this.ds = new DataSource(new Selection('multiple'));
        this.gridConnector = new GridConnector(this.ds);
        this.ds.setArray(this.data );


    }


}
```

attribute that can be used:

```text
  // ? = optional
  colWidth?: number;
  colRowTemplate?: string; (needs full html markup, see custom html)
  colHeaderTemplate?: string; (needs full html markup, see custom html)
  colField: string;
  colPinLeft?: boolean;
  colPinRight?: boolean;
  colHeaderName?: string;
  colAddLabelAttributes?: string;
  colAddFilterAttributes?: string;
  colAddRowAttributes?: string;
  colFilterMenu?: string;
  colLabelMenu?: string;
  colRowMenu?: string;
  colHidden?: boolean;
  colDragDrop?: string;
  colResizeable?: string;
  colSort?: string;
  colFilter?: string;
  colFilterTop?: boolean;
  colCss?: string;
  colType?: string;
```

