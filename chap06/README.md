#Internal function
To access the internal functions you use to object binded to ```v-grid-context``` you have seen in all samples earlier in the docs.

```javascript
myGrid = {}; //v-grid-context.bind="myGrid"  in <vgrid>
```

##Selection class
Funtions of the internal selection class

#####Get the selection
```javascript
var selection = this.myGrid.ctx.vGridSelection;
```


#####Number of rows in the selection
```javascript
selection.selectedRows;
```


#####Returns true if row in displayed rows is selected.
```javascript
selection.isSelected(row)
```


#####same as above just in binded collection
```javascript
selection.isSelectedMain(row)
```


#####deselects row passed in if selected in displayed rows
```javascript
selection.deSelect(row)
```

#####same as above just in binded collection
```javascript
selection.deSelectMain(row) 
```


#####add row to selection in displayed rows, if add to selection is not true, it replaces the old selection

```javascript
selection.select(row, addToSelection)
```

#####same as above just in binded collection

```javascript
selection.selectMain(row, addToSelection)
```


#####select rows in displayed selection, from-> to row

```javascript
selection.selectRange(start, end)
```
#####same as above just in binded collection
```javascript
selection.selectRangeMain(start, end) {
```


#####clears selection
```javascript
selection.reset()
```

#####returns array of index of the rows selected in in displayed rows
```javascript
selection.getSelectedRows()
```
#####same as above just in binded collection
```javascript
selection.getSelectedRowsMain()
```


#####pass in rows you want to select in displayed selection
```javascript
selection.setSelectedRows(indexArray)
```
#####same as above just in binded collection
```javascript
selection.setSelectedRowsMain(indexArray)
```

##Selection - filtering
Can only be used with local collection

#####show only selected
```javascript
this.myGrid.ctx.showOnlySelected()
```

#####show only the ones that isnt selectedselected
```javascript
this.myGrid.ctx.showOnlyNotSelected()
```

#####show only slected and not selected  (all)
```javascript
this.myGrid.ctx.showSelectedAndNotSelected()
```

##Scrolling

#####scroll to top
```javascript
this.myGrid.ctx.scrollTop()
```

#####scroll to x
```javascript
this.myGrid.ctx.setScrollTop(x)
```

#####scroll to bottom after you add/push new element into you array/collection
```javascript
this.myGrid.ctx.scrollBottomNext()
this.myCollection.push({name:"cool new person"});
```

#####get scrolltop
```javascript
let currentScrollTop = this.myGrid.ctx.getScrollTop()
```


##Other
#####activate overlay
```javascript
this.myGrid.ctx.setLoadingOverlay(true)
```

#####deactivate overlay
```javascript
this.myGrid.ctx.setLoadingOverlay(false)
```

#####sort by code
```javascript
let sortArray = [
      {attribute:"name", asc:false},
      {attribute:"number", asc:false}
    ]

this.myGrid.ctx.orderBy(sortArray);
```

#####redraws the grid (all is replaced)
```javascript
//if hidden during load you migh need to redraw so grid knows it bounds
this.myGrid.ctx.redrawGrid()
```

#####manually tell grid you have replaced collection/something and make it refresh all rows
```javascript
//set resetScrollToTop to true if you want it also to reset scroll
this.myGrid.ctx.columnChangeAndCollection(resetScrollToTop)
```

#####manually tell grid to rebuild columns/rows
needed when used with getColumns/setColumns
```javascript
this.myGrid.ctx.rebuildColumnsRows()
```

#####get internal column config
needed when used with getColumns
```javascript
let columnConfig = this.myGrid.ctx.getColumns()
```

#####set internal column config
needed when used with setColumns
```javascript
//need to call reGenerateColumns() after
// need to clear the custom hetml parts if you use get and set attributes and not just remove/add, else the html part will not be updated, since that overrides the other attributes
this.myGrid.ctx.setColumns(columnConfig)
```


##Remote

#####set data
```javascript
//see remote gist sample fro more usage
this.myGrid.ctx.setData(data)
```
