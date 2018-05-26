# v-grid-connector

Binds to gridConnector created in page

```text
v-grid-connector.bind="gridConnector"
```

App.js

```javascript
import { GridConnector } from 'aurelia-v-grid';
import { DataSource } from 'aurelia-v-grid';
import { Selection } from 'aurelia-v-grid';

export class App{

    constructor(){

        this.data =[
            {name:"Per"},
            {name:"Per"},
            {name:"Per"}]

        this.ds = new DataSource(new Selection('multiple'));
        this.gridConnector = new GridConnector(this.ds);
        this.ds.setArray(this.data );


    }


}
```

