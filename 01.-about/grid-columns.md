# grid columns

There are three options to create columns for the grid:

**"simple column HTML"** describes the situation where you create a `v-grid` element with some attributes and have `v-grid-col` elements inside it. This approach adds some properties ans styles by default to make it simple to use.

```markup
<v-grid>
  x-attributes

  <v-grid-col x-attributes></v-grid-col>
  <v-grid-col x-attributes></v-grid-col>
  <v-grid-col x-attributes></v-grid-col>

</v-grid>
```

> NOTE\* You can also bind array for making the columns, se attribute v-columns

**"custom column html"** option allows you use the `v-grid-col` and add `v-row-template` and `v-header-template` inside that to control what is displayed in column in row and header.

```markup
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

With custom html you can use custom attributes and css classes to have direct and easy control. We will cover the different custom attributes and what they do in another chapter.

