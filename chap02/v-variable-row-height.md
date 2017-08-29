# v-variable-row-height

Allows usage of variable row height
To use this add this to main element

```
v-variable-row-height='true'
```

In the data source you need to add `rowHeightCallback` function
This will be called when sorting/filtering/grouping/collapse and expand
This will be slower then just having own height for rows and groups and no callback

```
 this.ds = new DataSource(new Selection('multiple'), {
    rowHeight: 50,
    groupHeight: 25,
    rowHeightCallback: (x: any) => {
        //used the row data to define how tall it needs to be
        if (x.index % 3 === 0) {
            return 35;
        } else {
            return 50;
        }
    }
});
        ```



