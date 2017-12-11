# Elementos

Elementos são coisas dentro do seu componente.

![](images/component-elements.png)

## Nomeando elementos
Cada componente pode ter elementos. Eles devem ser classes que são apenas **uma palavra**.

```scss
.search-form {
  > .field { /* ... */ }
  > .action { /* ... */ }
}
```

## Seletores de elementos
Prefira usar o seletor de filho `>` sempre que possível. Isto evita conflitos através de componentes aninhados e funciona melhor do que seletores descendentes.

```scss
.article-card {
  .title     { /* okay */ }
  > .author  { /* ✓ melhor */ }
}
```

## Com várias palavras
Para classes que precisam de duas ou mais palavras, concatene-os sem traços ou travessões.

```scss
.profile-box {
  > .firstname { /* ... */ }
  > .lastname { /* ... */ }
  > .avatar { /* ... */ }
}
```

## Evite seletores de tags
Use classes sempre que possível. Os seletores de tag são bons, mas podem ter uma pequena penalidade no desempenho e não são tão descritivos.

```scss
.article-card {
  > h3    { /* ✗ evitar */ }
  > .name { /* ✓ melhor */ }
}
```

Nem todos os elementos devem sempre parecer os mesmos. Variantes podem ajudar.
[Continue →](variants.md)
<!-- {p:.pull-box} -->
