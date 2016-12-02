# col-filter

Adds filter to header, combine this with ```col-filter-top="true"``` if you dont want them under label

![](../vgridanimation/filtertop.png)

When using booleans you would need a valueConverter. Define it like this:

```html
<v-grid-col col-field="isReleased | bool" col-type="checkbox" col-filter="field: isReleased; converter: bool;"></v-grid-col>
```

The `converter` property of `col-filter` takes the **name** of a value converter. It will internally be trandformed to (in the above example) `BoolValueConverter`.
