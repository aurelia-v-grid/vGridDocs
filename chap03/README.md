# How to use:

This chapter we will go into the 3 ways to make columns.
 * simple html
 * column.bind
 * custom html

The grid also has an element called ```<v-grid-row-repeat>``` which doesn't define any columns. This can be used when you have a form you want to repeat for each row.

Before we go into details how to make the columns, lets look at what attributes the main element has.

##### ```<v-grid>``` attributes:
* v-grid-context
* v-collection  (required)
* v-current-entity
* v-columns
* v-row-height
* v-header-height
* v-footer-height
* v-multi-select
* v-manual-sel
* v-loading-threshold
* v-remote-index
* v-row-on-draw
* v-row-onclick
* v-row-ondblclick
* v-event-onremote
* v-only-custom
* v-attribute-observe

---
##### Attibute use:

The code below shows all attributes. You would not use all of these at the same time, but have all here so you can see how to use it:

```
<v-grid
    class="col-md-6"
    style="height:350px"
    v-row-height="25"
    v-header-height="50"
    v-row-onclick.delegate="singleClick($event.detail)"
    v-row-ondblclick.delegate="singleDblClick($event.detail)"
    v-current-entity.bind=myCurrentEntity
    v-multi-select="true"
    v-remote-index="id"
    v-event-onremote.call="callRemoteServer($event)"
    v-remote-collection-event.delegate="remotePagerEvent($event.detail)"
    v-local-collection-event.delegate="collectionEvent($event.detail)"
    v-language.bind=myLang
    v-hide-pager-info="false"
    v-attribute-observe="name,salery"
    v-only-custom="false"  //default is true
    v-custom-pager="<my-pager-element></my-pager-element>"
    v-row-on-draw.call="onRowDraw($event)"
    v-collection.bind=myCollection
    v-columns.bind=columnSetup
    v-grid-context.bind=myGrid>

    //columns!!!

</v-grid>

```

---

##### v-collection (REQUIRED)

The main collection to be used with grid
You are required to add this for grid to work

##### v-grid-context

Grid context, under ctx here you will have access to all internal methods
You are required to add this for grid to work


##### v-current-entity

Current selected row of the grid, use this to bind to inputs etc
You are required to add this for grid to work

##### v-columns

This is only used when you defined columns with array not html
If you defined columns using ```v-grid-col``` then the grid will overlook this attribute

##### v-row-height

Height of the row, default is 50px

##### v-header-height

Height of header, default = 0px

##### v-footer-height

Height of footer, default = 0px

##### v-multi-select
False = single, true = multi, default = no selection

##### v-manual-sel

This need to be tru if you want to use selection column.
When using simple html og column bind this is set to true by grid if one of the columns are type selection

##### v-row-onclick

Register for row click event

##### v-row-ondblclick

Register for row dblclick event

##### v-loading-threshold

How large collection need to be before loading overlay displays on filter/sorting
For local data you could have it a 10 000, default is -1 (on all the time)

##### v-remote-index

For selection the grid added a unique index to the grid, if you collection have unique data column then you can define that so the grid does not add anything.
For remote data this is very useful since it will remember selection with paging also

##### v-row-on-draw

Callback when drawing row

##### v-event-onremote

Callback for filter/sorting and paging
You need to set footerheight to min 25px for it to show if you want to use it

##### v-hide-pager-info

hides the page info under buttons is set to true, default = false

##### v-custom-pager

for setting custom element instead of the internal pager, you will need to copy mine and have some of the default function there for this to work

##### v-local-collection-event

Event that gets called when total collection length changes, internal collection, or selection

##### v-remote-collection-event

callback for when pager is set, gives you page, pages, length(total), pageSize(limit)

##### v-only-custom

stops grid from adding a few of the custom attributes it does in the clumn on simple html & column.bind, these are:
v-key-move, v-image-fix, v-resize-col, v-drag-drop-col, v-observe-field

##### v-attribute-observe

setting observer on current entity attributes for updates to current row

##### v-language

bind object to set own text/language for internal menus and pager



```
//object with the default, if you skip some then it used the internal defaults
//you can copy this and modify the parts you want
object = {
  
  //pager buttons
  pagerBtnNext:"Next",
  pagerBtnLast:"Last",
  pagerBtnFirst:"First",
  pagerBtnLast:"Last",
  
  //pager text
  pagerStringPage:"Page ",
  pagerStringOf:" of ",
  pagerStringTotalEntities:", Total entities:",
  pagerStringPageSize:", page size ",
  
  
  //main header menu
  menuMainHeaderOptions:"Options",
  menuMainHeaderClearCell:"Clear cell",
  menuMainHeaderClearAllCells:"Clear All Cells",
  menuMainHeaderShowAll:"Show all (keep filter text)",
  menuMainHeaderSetFilter:"Set Filter",
  
  //filter sub menu
  menuFilterHeaderSetFilter:"Set filter",
  menuFilterHeaderEquals:"equals",
  menuFilterHeaderLessThanOrEq:"less than or eq",
  menuFilterHeaderGreaterThanOrEq:"greater than or eq",
  menuFilterHeaderLessThan:"less than",
  menuFilterHeaderGreaterThan:"greater than",
  menuFilterHeaderContains:"contains",
  menuFilterHeaderNotEqualTo:"not equal to",
  menuFilterHeaderDoesNotContain:"does not contain",
  menuFilterHeaderBeginsWith:"begins with",
  menuFilterEndsWith:"ends with"

  //row menu
  menuRowOptions:"Options",
  menuRowCopyCellValue:"Copy cell value",
  menuRowCopyPasteIntoCell:"Paste into cell/selected rows"

}
```


