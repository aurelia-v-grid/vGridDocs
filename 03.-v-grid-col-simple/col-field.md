# col-field

Field from array row to put in data from \(required\)

You should add value converter to numbers and booleans if you dont want inputs to mess them up when html gets binned with html

`<v-grid-col col-field="bool | booleanFormatter"></v-grid-col>`

`<v-grid-col col-field="number | numberFormatter"></v-grid-col>`

Sample of a value converter

`<require from="./utils/valueConverter"></require>`

```text
export class NumberFormatterValueConverter {
  public toView(value: any) {
    if (value) {
      return value;
    } else {
      return value;
    }
  }

  public fromView(value: any) {
    if (value) {
      let check = value * 1;
      if (isNaN(check)) {
        return value;
      } else {
        return value * 1;
      }

    } else {
      return value;
    }
  }
}

export class BooleanFormatterValueConverter {
  public toView(value: any) {
    if (value) {
      return value;
    } else {
      return value;
    }
  }

  public fromView(value: any) {

    if (typeof value === 'string') {
      value = value.toLowerCase();
      switch (value) {
        case 'true':
          value = true;
          break;
        case 'false':
          value = true;
          break;
        default:
          value = false;
      }
    }


    return value;
  }
}
```

