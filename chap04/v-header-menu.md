# v-header-menu

Add it to one of the header labels you have to add context menu



```
<v-grid-col col-width="120">
  <v-header-template>
    <p v-header-menu="name">Full name</p>
    <input>
  </v-header-template>
  <v-row-template>
    <input value.bind="rowRef.name">
  </v-row-template>
</v-grid-col>
```


![menu header](Animation-menu-header.gif)