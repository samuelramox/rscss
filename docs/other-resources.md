# Outros recursos

 * [ITCSS](https://speakerdeck.com/dafed/managing-css-projects-with-itcss#49) ("Inverted Triangle CSS") é um bom complemento para qualquer estrutura rscss.
 * [rsjs](http://ricostacruz.com/rsjs/) ("Reasonable Standard of JavaScript Structure") é uma documentação em andamento para estruturar JavaScript em sites básicos.

Outras soluções
---------------

### BEM
[BEM] é legal, mas alguns podem se irritar com a sua sintaxe pouco convencional. RSCSS praticamente segue as convenções BEM, apenas com uma sintaxe diferente.

```html
<!-- BEM -->
<form class='site-search site-search--full'>
  <input  class='site-search__field' type='text'>
  <button class='site-search__button'></button>
</form>
```

```html
<!-- rscss -->
<form class='site-search -full'>
  <input  class='field' type='text'>
  <button class='button'></button>
</form>
```

## Terminologias

Os mesmos conceitos existem de maneiras semelhantes em outras ideologias de estrutura CSS.

| RSCSS     | BEM      | SMACSS        |
| ---       | ---      | ---           |
| Component | Block    | Module        |
| Element   | Element  | Sub-Component |
| Layout    | ?        | Layout        |
| Variant   | Modifier | Sub-Module & State |

[BEM]: http://bem.info/
[Smacss]: https://smacss.com/
