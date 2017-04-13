# v-filter-observer

```
v-filter-observer="field:name; operator:*; converter:num; value:rowref.name"
```

Adds bindables to value  
Triggers filter when value changes



```
<v-header-template>
  <md-range 
    v-filter-observe="field:index;operator:<;value.bind:rangeValue;converter:numberFormatter" md-value.bind="rangeValue">
  </md-range>
</v-header-template>
```



