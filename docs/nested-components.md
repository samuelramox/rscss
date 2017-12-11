# Componentes aninhados

![](images/component-nesting.png)

```html
<div class='article-link'>
  <div class='vote-box'>
    ...
  </div>
  <h3 class='title'>...</h3>
  <p class='meta'>...</p>
</div>
```

Às vezes é necessário aninhar componentes. Aqui estão algumas orientações para fazer isso.

## Variantes
Um componente pode precisar aparecer de maneira diferente quando aninhado em outro componente. Evite modificar o componente aninhado através do componente que o contém.

```scss
.article-header {
  > .vote-box > .up { /* ✗ evite isso */ }
}
```

  Em vez disso, prefira adicionar uma variante ao componente aninhado e aplicá-la a partir do componente que o contém.

```html
<div class='article-header'>
  <div class='vote-box -highlight'>
    ...
  </div>
  ...
</div>
```

```scss
.vote-box {
  &.-highlight > .up { /* ... */ }
}
```

## Simplificando componentes aninhados
Às vezes, ao aninhar componentes, seu código pode ficar sujo:

```html
<div class='search-form'>
  <input class='input' type='text'>
  <button class='search-button -red -large'></button>
</div>
```

Você pode simplificar isso usando a função `@extend` do seu pré-processador CSS:

```html
<div class='search-form'>
  <input class='input' type='text'>
  <button class='submit'></button>
</div>
```

```scss
.search-form {
  > .submit {
    @extend .search-button;
    @extend .search-button.-red;
    @extend .search-button.-large;
  }
}
```

E quanto a elementos que se repetem, como as listas? Saiba mais sobre Layouts.
[Continue →](layouts.md)
<!-- {p:.pull-box} -->
