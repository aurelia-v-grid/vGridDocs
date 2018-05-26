# v-menu-sort

```text
<ul if.bind="sortMenu && !filterOptionsMenu" class="avg-menu__items">
    <li class="avg-menu__item">
    <p click.delegate="menuClick('sort','asc', $event)" class="avg-menu__link">
           <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
            <path d="M7.4 6L3 10h1.5L8 7l3.4 3H13L8.5 6h-1z"/>
          </svg> ${this.menuStrings.sortAscending}
    </p>
    </li>
    <li class="avg-menu__item">
    <p click.delegate="menuClick('sort','desc', $event)" class="avg-menu__link">
        <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
            <path d="M7.4 10L3 6h1.5L8 9.2 11.3 6H13l-4.5 4h-1z"/>
        </svg> ${this.menuStrings.sortDescending}
    </p>
    </li>
</ul>

`
```

![](../.gitbook/assets/v-menu-main-types.png)

