



```html
<v-menu-chooser>
<ul if.bind="hideshow && !optionsMenu" class="avg-menu__items">
        <li class="avg-menu__item">
        <p click.delegate="menuClick('column','options', $event)" class="avg-menu__link">
            <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
                <path d="M7.4 4.8v2.7H4.7v1h2.7v3h1v-3h2.8v-1H8.5V4.8h-1z"/>
              </svg> ${menuStrings.columnChooser}
        </p>
        </li>
</ul>
</v-menu-chooser>

```



```html
<v-menu-chooser-options>
    <ul if.bind="columnOptionsMenu" class="avg-menu__items">
        <li class="avg-menu__item">
            <p click.delegate="menuClick('option','Back', $event)" class="avg-menu__link">
                <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
                   <path d="M8.7 4v1.2L5 7.5h8v1H5l3.7 2.2V12L3 8.4v-1L8.7 4z"/>
                </svg> ${menuStrings.back}
            </p>
        </li>
        <div repeat.for="item of columnsHidden">
            <li class="avg-menu__item">
                <avg-drag-helper v-drag-drop-col="title.bind:item.title" data-avg-type="chooser"  data-avg-config-col="${item.no}">
                    <p class="avg-menu__link">
                        <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
                            <path show.bind="!rowRef.__groupExpanded" d="M7.4 4.8v2.7H4.7v1h2.7v3h1v-3h2.8v-1H8.5V4.8h-1z"/>
                        </svg>
                        ${item.title}
                    </p>
                </avg-drag-helper>
            </li>
        </div>
    </ul>
</v-menu-chooser-options>


```



