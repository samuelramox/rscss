# Estrutura CSS

## Um componente por arquivo
É recomendável colocar cada componente em seu próprio arquivo.

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

## Use o padrão global
Em sass-rails e stylus, isso facilita incluir todos os componentes:

  ```scss
  @import 'components/*';
  ```

## Evite o excesso de aninhamento
Não use mais do que 1 nível de aninhamento. É fácil se perder com muito aninhamento.

  ```scss
  /* ✗ Avoid: 3 levels of nesting */
  .image-frame {
    > .description {
      /* ... */

      > .icon {
        /* ... */
      }
    }
  }

  /* ✓ Better: 2 levels */
  .image-frame {
    > .description { /* ... */ }
    > .description > .icon { /* ... */ }
  }
  ```
