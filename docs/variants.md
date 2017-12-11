# Variantes

Os componentes podem ter variantes. Os elementos também podem ter variantes.

![](images/component-modifiers.png)

<br>

## Nomeando variantes
Nomes de classes para variantes devem ser prefixados por um traço (`-`).

  ```scss
  .like-button {
    &.-wide { /* ... */ }
    &.-short { /* ... */ }
    &.-disabled { /* ... */ }
  }
  ```

## Variantes de elementos
Os elementos também podem ter variantes.

  ```scss
  .shopping-card {
    > .title { /* ... */ }
    > .title.-small { /* ... */ }
  }
  ```

## Prefixados com traço
Traços são o prefixo preferido para as variantes.

  * Evita ambiguidades com elementos.
  * Uma classe CSS só pode começar com uma letra, `_` ou `-`.
  * Traços são mais fáceis de digitar do que sublinhados.
  * Isso se assemelha a switches nos comandos UNIX (`gcc -O2 -Wall -emit-last`).

Como você lida com elementos complexos? Aninhe eles.
[Continue →](nested-components.md)
<!-- {p:.pull-box} -->
