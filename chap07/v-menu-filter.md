# ```<v-menu-filter>```

```
<ul if.bind="filterMainMenu && !filterOptionsMenu" class="avg-menu__items">
    <li class="avg-menu__item">
    <p click.delegate="menuClick('filter','showall', $event)" class="avg-menu__link">
        <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
            <path d="M7.4 4.8v2.7H4.7v1h2.7v3h1v-3h2.8v-1H8.5V4.8h-1z"/>
          </svg> ${this.menuStrings.showAll}
    </p>
    </li>
    <li class="avg-menu__item">
    <p click.delegate="menuClick('filter','clear', $event)" class="avg-menu__link">
        <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
            <path d="M4.8 7.5h6.5v1H4.8z">
          </svg> ${this.menuStrings.clearCurrent}
    </p>
    </li>
    <li class="avg-menu__item">
    <p click.delegate="menuClick('filter','clearall', $event)" class="avg-menu__link">
        <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
            <path d="M4.8 7.5h6.5v1H4.8z">
          </svg> ${this.menuStrings.clearAll}
    </p>
    </li>
    <li class="avg-menu__item">
    <p click.delegate="menuClick('filter','options', $event)" class="avg-menu__link">
        <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
            <path d="M7.3 4v1.2L11 7.5H3v1h8l-3.7 2.2V12L13 8.4v-.8L7.3 4z"/>
          </svg> ${this.menuStrings.chooseOperator}
    </p>
    </li>
</ul>
```
![](../vgridanimation/v-menu-main-types.png)


