# v-i18n

To translate menus and placeholders, use the `this.gridConnector.triggerI18n();` to trigger the grid to ask for new keys/translation if you change language

add to v-grid element

```html
v-i18n.call="translateI18n($event)"
```

quick sample of code in you page \(boring translation... but something\)

```javascript
// this is the i18N translation
  public translateI18n(key: string) {
    return this.testString;
  }

  //this is called by my button... not very good
  public translate() {
    if (this.testString === 'cool') {
      this.testString = 'yay';
    } else {
      this.testString = 'cool';
    }
    // this will trigger the grid to ask for every translation key
    this.gridConnector.triggerI18n();
  }
```

Default keys inside the grid

```javasrcipt
      close: 'Close',
      pinLeft: 'Pin left',
      pinRight: 'Pin Right',
      groupBy: 'Group By',
      sortAscending: 'Sort Ascending',
      sortDescending: 'Sort Descending',
      showAll: 'Show All',
      clearCurrent: 'Clear Current',
      clearAll: 'Clear All',
      chooseOperator: 'Choose Operator',
      back: 'Back',
      equals: 'Equals',
      lessThanOrEqual: 'Less than or equal',
      greaterThanOrEqual: 'Greater than or equal',
      lessThan: 'Less than',
      greaterThan: 'Greater than',
      contains: 'Contains',
      notEqualTo: 'Not equal to',
      doesNotContain: 'Does not contain',
      beginsWith: 'Begins with',
      endsWith: 'Ends with',
      loading: 'loading',
      columnChooser: 'Column Chooser',
      copy: 'Copy cell value',
      paste: 'Paste into cells'
```



