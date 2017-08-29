# ```<V-GRID>``` 

###Attributes

See the next articles for more information on what you can use and how
For own custom grouprow height compared to regular row see the v-variable-row-height

```html
<v-grid>
  v-multi-select="true" 
  v-grid-connector.bind="gridConnector" 
  v-row-height="25" 
  v-header-height="50" 
  v-panel-height="25"
  v-footer-height="25"
  v-data-delay="200"
  v-row-onclick.delegate="singleClick($event.detail)"
  v-row-ondblclick.delegate="dblClick($event.detail)"
  
  <v-grid-col></v-grid-col>
  <v-grid-col></v-grid-col>
  <v-grid-col></v-grid-col>
  
</v-grid>
```