# ```<v-grid-row-repeat>```

### custom group row

Is implemented, just not tested very much

Instead of using ```<v-grid-col></v-grid-col>``` you add:

```<v-grid-row-repeat> whatever html you want </v-grid-row-repeat>>```

This will use entire row for diaplaying data, nice for displaying forms when you really dont need columns

you can also here defined what goes into header and what goes into row

```
<v-grid-row-repeat>
  <v-header-template>
          <--------I go into header-------->
  </v-header-template>
  <v-row-template>
         <--------I go into row------------>
  </v-row-template>
</v-grid-row-repeat>

```