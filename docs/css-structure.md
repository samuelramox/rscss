# Estrutura CSS

## Um componente por arquivo
Coloque cada componente em seu próprio arquivo.

  ```scss
  /* css/components/search-form.scss */
  .search-form {
    > .button { /* ... */ }
    > .field { /* ... */ }
    > .label { /* ... */ }

    // variants
    &.-small { /* ... */ }
    &.-wide { /* ... */ }
  }
  ```

## Use padrões globais
Em sass-rails e stylus, a instrução abaixo inclui todos os componentes facilmente:

  ```scss
  @import 'components/*';
  ```

## Evite o excesso de aninhamento
Não use mais do que 1 nível de aninhamento. É fácil se perder com muito aninhamento.

  ```scss
  /* ✗ Evite: 3 níveis de aninhamento */
  .image-frame {
    > .description {
      /* ... */

      > .icon {
        /* ... */
      }
    }
  }

  /* ✓ Melhor: 2 níveis */
  .image-frame {
    > .description { /* ... */ }
    > .description > .icon { /* ... */ }
  }
  ```
