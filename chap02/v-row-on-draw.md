# v-row-on-draw

Can be used to set tempRef data to use for  styling etc

Add to ```<v-grid>``` element:
```
v-row-on-draw.call="onRowDraw($event)"
```


```
 onRowDraw(data) {
    if (data) {
      if (data.tempRef) {
        if (data.tempRef.number > 100) {
          data.tempRef.numberColor = "green";
          data.tempRef.numberFont = "normal";
        } else {
          data.tempRef.numberColor = "red";
          data.tempRef.numberFont = "bold";
        }
      }
    }
  }
  ```
  
  in row you can add css attribute
  
  ```
  col-css="color:${tempRef.numberColor};font-weight:${tempRef.numberFont}"
  ```