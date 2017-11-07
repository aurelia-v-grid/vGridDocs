# gridConnector

Methods in default **GridConnector**, see the "About" for how to create gridConnector



----

######getColConfig(): ColConfig[]

```
let columnConfigArray = this.gridConnector.getColConfig();
```

######setColConfig(colconfig: ColConfig[]): void

```
this.gridConnector.getColConfig(columnConfigArray);

//resets to default (html, or when grid loaded of no html)
this.gridConnector.getColConfig(null)

```


Interface
```
export interface ColConfig {
  [key: string]: any;
  colWidth?: number;
  colRowTemplate?: string;
  colHeaderTemplate?: string;
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
  __colSortHelper?: number;
  __colHeaderTemplateGenerated?: string;
  __colRowTemplateGenerated?: string;
}
```

---

######getTopRow(): number
* Can be used to get current scrolltop
* Use this with setInitTop if you want to go between master/detail and have same rows displayed

---


######triggerI18n(): void
* Forces grid to try and update language

---


######raiseEvent(name: string, data = {}): void
* Raise event on the grid element, usefull for overriding default behavior
* I really dont want much of this, use at own expense

---

######setInitTop(top: number): void
* Set scroll value grid will use when it loads
* Useful for when going back from a detail view

