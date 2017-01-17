# col-filter

Adds filter to header, combine this with ```col-filter-top="true"``` if you dont want them under label

![](../vgridanimation/filtertop.png)

When using booleans you would need a valueConverter. Define it like this:

**Simple with operator "equal to"**

```html
col-filter="field: name;">
```
**
Operator**

```html
col-filter="field: name; operator:*">
```

* '=':  equal
* '<=': less than or equal to
* '>=': greater than or equal to
* '<':  less than
* '>':  greater than
* '*':  contains
* '!=': not equal to
* '!*': does not contain
* '*=': begin with
* '=*': end with


**Convert**
```html
col-filter="field: isReleased; converter: bool;">
```
The `converter` property of `col-filter` takes the **name** of a value converter. It will internally be trandformed to (in the above example) `BoolValueConverter`.


**Trigger after on key down**
```html
col-filter="field: name; keydown:onKeyDown>
```










