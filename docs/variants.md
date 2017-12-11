# Variantes

Componentes podem ter variantes. Elementos também podem ter variantes.

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
Elementos também podem ter variantes.

  ```scss
  .shopping-card {
    > .title { /* ... */ }
    > .title.-small { /* ... */ }
  }
  ```

## Prefixos com traços
Traços são o prefixo recomendados para as variantes.

  * Evita ambiguidades com elementos.
  * Uma classe CSS só pode começar com uma letra, `_` ou `-`.
  * Traços são mais fáceis de digitar do que travessões.
  * Isso se assemelha a switches nos comandos UNIX (`gcc -O2 -Wall -emit-last`).

Como você lida com elementos complexos? Aninhando.
[Continue →](nested-components.md)
<!-- {p:.pull-box} -->
