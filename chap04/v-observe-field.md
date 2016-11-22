# v-observe-field
Add to make data flow between input row and current entity

```
<v-grid-col col-width="120">
  <v-header-template>
    <p>Full name</p>
    <input>
  </v-header-template>
  <v-row-template>
    <input  v-observe-field="name" value.bind="rowRef.name">
  </v-row-template>
</v-grid-col>
```

![observe](Animation-observe.gif)