# Layouts

![](images/layouts.png)

## Evite propriedades de posicionamento
Componentes devem ser feitos de forma a serem reutilizáveis ​​em diferentes contextos. Evite colocar essas propriedades em componentes:

  * Posicionamento (`position`, `top`, `left`, `right`, `bottom`)
  * Flutuadores (`float`, `clear`)
  * Margens (`margin`)
  * Dimensões (`width`, `height`) *

## Dimensões fixas

A exceção a isso podem ser os elementos que possuem largura/alturas fixas, como avatares e logotipos.

## Definir posicionamento nos pais

Se você precisar definir isso, tente defini-los no contexto em que estão. No exemplo abaixo, observe que width e float são aplicados no componente da *lista*, e não no componente em si.

  ```css
  .article-list {
    & {
      @include clearfix;
    }

    > .article-card {
      width: 33.3%;
      float: left;
    }
  }

  .article-card {
    & { /* ... */ }
    > .image { /* ... */ }
    > .title { /* ... */ }
    > .category { /* ... */ }
  }
  ```

Como você aplica margens fora de um layout? Experimente com os Helpers.
[Continue →](helpers.md)
<!-- {p:.pull-box} -->
