# checkbox


####Sample code from picture below

**checkbox** 
```
<v-grid-col col-width="70">
  <v-header-template>
    <input class="vgrid-row-checkbox-50" v-header-menu="bool" type="checkbox" v-filter="bool|=">
    <p class="vgrid-label-bottom" v-sort="bool">Bool</p>
  </v-header-template>
  <v-row-template>
    <input class="vgrid-row-checkbox-100" v-row-menu="bool" type="checkbox" checked.bind="rowRef.bool">
  </v-row-template>
</v-grid-col>
```

(todo: replace picture, "vgrid-" needs to be "avg-")
![classes image](cssclasses.png)