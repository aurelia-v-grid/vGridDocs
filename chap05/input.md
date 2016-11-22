# input

####Sample code from picture below

**input**
```
<v-grid-col col-width="100">
  <v-header-template>
    <input v-header-menu="number" class="vgrid-header-input-top" v-filter="number|>=" value.bind="tempRef.number">
    <p class="vgrid-label-bottom" v-sort="number">Number</p>
  </v-header-template>
  <v-row-template>
    <input v-row-menu="number" class="vgrid-row-input" 
      value.bind="rowRef.number | numberFormat  & updateTrigger:'blur':'paste'"
      css="color:${tempRef.numberColor};font-weight:${tempRef.numberFont}">
     </v-row-template>
</v-grid-col>
```

(todo: replace picture, "vgrid-" needs to be "avg-")
![classes image](cssclasses.png)