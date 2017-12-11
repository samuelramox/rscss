# Elementos

Elementos são coisas dentro do seu componente.

![](images/component-elements.png)

## Nomeando elementos
Cada componente pode ter elementos. Eles devem ter classes que são apenas **uma palavra**.

```scss
.search-form {
  > .field { /* ... */ }
  > .action { /* ... */ }
}
```

## Seletores de elementos
Prefira usar o `>` seletor de filhos sempre que possível. Isto evita herança através de componentes aninhados, e funciona melhor do que seletores descendentes.

```scss
.article-card {
  .title     { /* okay */ }
  > .author  { /* ✓ better */ }
}
```

## Com múltiplas palavras
Para aqueles que precisam de duas ou mais palavras, concatene-os sem traços ou sublinhados.

```scss
.profile-box {
  > .firstname { /* ... */ }
  > .lastname { /* ... */ }
  > .avatar { /* ... */ }
}
```

## Evite seletores de tag
Use classes sempre que possível. Os seletores de tag são bons, mas podem ter uma pequena penalidade de desempenho e podem não ser tão descritivos.

```scss
.article-card {
  > h3    { /* ✗ avoid */ }
  > .name { /* ✓ better */ }
}
```

Nem todos os elementos devem sempre parecer os mesmos. Variantes podem ajudar.
[Continue →](variants.md)
<!-- {p:.pull-box} -->
