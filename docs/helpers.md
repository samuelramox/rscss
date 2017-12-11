# Helpers

Para classes de propósito geral que pretendem anular os valores, coloque-os em um arquivo separado e nomeie-os com um sublinhado. Eles são coisas que tipicamente são marcadas com *!important*. Use-os com *muita* moderação.

```css
._unmargin { margin: 0 !important; }
._center { text-align: center !important; }
._pull-left { float: left !important; }
._pull-right { float: right !important; }
```

## Nomeando helpers
Prefixe os nomes destas classes com um sublinhado. Isso facilitará a diferenciação dos modificadores definidos no componente. Os sublinhados também parecem um pouco feios, o que é um efeito colateral intencional: o uso de muitos helpers deve ser desencorajado.

  ```html
  <div class='order-graphs -slim _unmargin'>
  </div>
  ```

## Organizando helpers
Coloque todos os helpers em um arquivo chamado `helpers`. Você pode separá-los em múltiplos arquivos, mas é preferível manter o número de helpers no mínimo.
