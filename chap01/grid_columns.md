# grid columns


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
We will cover the different custom attributes and what they do in another chapter.

