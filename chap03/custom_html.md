# Custom Column HTML
* [Gist demo with all enabled](https://gist.run/?id=6ad85edc11f552f2afde0bf19bf14333)

Works almost just the same as simple column HTML

Main difference is when you define the columns you add html inside the ```V-grid-col```.
Only attribute that is common for this and "simple column HTML" is the ```col-width```

You can mix "custom HTML" and "simple column HTML"

When you define you columns you now get 2 more options, controlling what goes into header part and row

```
<v-grid-col col-width="30">
  <v-header-template>
          <--------I go into header-------->
  </v-header-template>
  <v-row-template>
         <--------I go into row------------>
  </v-row-template>
</v-grid-col>

```

Controlling filters, sorting and add dragdrop is done by custom attributes.
See chapter 04 for details on what/how.

For a more complete sample open the demo

