todo, update, code below is changed


```
<v-grid-group-row>
          <i click.delegate="changeGrouping(rowRef)"
            class="avg-fa avg-fa-${rowRef.__groupExpanded ? 'minus':'plus'}-square-o"
            aria-hidden="true">
          </i>
          &nbsp;${rowRef.__groupName} (${rowRef.__groupTotal})
 </v-grid-group-row>
 ```
 