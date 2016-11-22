#About the grid

This grid operates on a bound array of items and a current entity which holds the selected item.
The grid observes the array bound to it and creates an internal clone it uses for displaying data.

> The array needs to be initialized as an object array, current entity as an empty object {}

When someone uses filter it takes the main array and uses `[].filter()` on it. The result of this replaces the internal clone, so it doesn't mess with the array bound to the grid.
On sorting it just sorts the internal clone, no the bound collection.

When someone updates a field on the internal array, this change will be reflected by the array bound to the grid.

The grid has a current entity object you bind to the grid, that's the one you use with your inputs. When you select a row in the grid it displays that row data in the object, so inputs get updated.
The grid has an attribute to observe bound properties. When updating data the input/row gets updated on every key touch.

There are three options to create columns for the grid:

**"simple column HTML"** describes the situation where you create a `v-grid` element with some attributes and have `v-grid-col` elements inside it. This approach adds some properties ans styles by default to make it simple to use.

```html
<v-grid>
  x-attributes
  
  <v-grid-col x-attributes></v-grid-col>
  <v-grid-col x-attributes></v-grid-col>
  <v-grid-col x-attributes></v-grid-col>
  
</v-grid>
```


**"column.bind"** describes the situation where you bind an array to one of the attributes in the main ```v-grid``` element. This option is provided for the case where you do not want to write any HTML code at all and do the most of your actions in your model.

```html
<v-grid>
  x-attributes
  column.bind="nameOfMyColumnArray"
</v-grid>
```

**"custom column html"** option allows you use the `v-grid-col` and add `v-row-template` and `v-header-template` inside that to control what is displayed in column in row and header.

```html
<v-grid>
  x-attributes
  
  <v-grid-col>
    <v-header-template> custom html </v-header-template>
    <v-row-template> custom html </v-row-template>
  </v-grid-col>
  
  <v-grid-col>
    <v-header-template> custom html </v-header-template>
    <v-row-template> custom html </v-row-template>
  </v-grid-col>
  
  <v-grid-col>
    <v-header-template> custom html </v-header-template>
    <v-row-template> custom html </v-row-template>
  </v-grid-col>
  
</v-grid>
```

With custom html you can use custom attributes and css classes to have direct and easy control.
We will cover the different custom attributes and what they do in another chapter. (**link to chapter**)





















