# &lt;cpol-currency&gt;

`<cpol-currency>` is a polymer currency generator tools. It convert your input amount to be currency formated.

### How to install:
`bower install --save cpol-currency`

### Simple example to use &lt;cpol-currency&gt;:
```html
<cpol-currency amount='10'></cpol-currency>
```

### You can use data binding to insert the amount and the type can be number or string.
```html
  <template>
    <style>
      :host {
        display: block;
      };
    </style>
    ...
    <cpol-currency amount=[[userMoney]]></cpol-currency>
    ...
  </template>
  <script>
    Polymer({
      ...
      properties: {
        ...
        userMoney: {
          type: string,
          value: '1500',
        },
        ...
      },
      ...
    });
  </script>
```

### You can also change number of decimal, character for decimal separator and thousand separator, currency prefix and suffix for currency symbol.
```html
  <template>
    <style>
      :host {
        display: block;
      };
    </style>
    ...
    <cpol-currency
      decimal-separator=','
      value-separator='.'
      currency-prefix='Rp'
      amount=[[userMoneyDecimal]]>
    </cpol-currency>
    ...
  </template>
  <script>
    Polymer({
      ...
      properties: {
        ...
        userMoneyDecimal: {
          type: Number,
          value: 1350.35,
        },
        ...
      },
      ...
    });
  </script>
```

### Properties you can use:
Properties | Description | Type | Default
--- | --- | --- | ---
amount | Amount of money that will be converted to currency format | Number or String | 0
fixed | Number of decimal will be converted | Number | 2
decimal-separator | Character for separate decimal | String | '.'
value-separator | Character for separate thousand in amount | String | ','
currency-prefix | Prefix character of currency symbol | String | '$'
currency-suffix | Suffix character of currency symbol | String | ''