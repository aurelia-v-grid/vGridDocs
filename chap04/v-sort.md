# v-sort
For adding sort icon and making the grid sort when header label is clicked

```html
<v-grid-col col-width="120">
  <v-header-template>
    <p  v-sort="name" >Full name</p>
  </v-header-template>
  <v-row-template>
    <input value.bind="rowRef.name">
  </v-row-template>
</v-grid-col>

```

![](animation-sorting.gif)