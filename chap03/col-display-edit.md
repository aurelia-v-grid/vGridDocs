###col-display-edit

one value-converter when displaying date and one for when editing

That way you can have formatted value during display and show entire value when editing



```
<v-grid-col
         col-filter-menu="filter:number"
         col-label-menu="sort:number"  
         col-width="100"
         col-css="color:${tempRef.numberColor};font-weight:${tempRef.numberFont}"
         col-sort="field:number" 
         col-filter="field:number;operator:<" 
         col-display-edit="field:number;edit:editFormatNumber;display:displayFormatNumber"
         col-field="number" 
>
```
     
![](/assets/col-display-edit.gif)    
