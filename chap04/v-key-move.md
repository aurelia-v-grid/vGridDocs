# v-key-move
Add to make column tab-able, you can also use page up/down and arrow keys up/down


```
<v-grid-col col-width="120">
  <v-header-template>
    <p>Full name</p>
    <input>
  </v-header-template>
  <v-row-template>
    <input  v-key-move value.bind="rowRef.name">
  </v-row-template>
</v-grid-col>
```