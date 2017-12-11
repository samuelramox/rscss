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
Um componente pode precisar aparecer de uma certa maneira quando aninhado em outro componente. Evite modificar o componente aninhado, alcançando ele através do componente que o contém.

```scss
.article-header {
  > .vote-box > .up { /* ✗ avoid this */ }
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
Às vezes, ao aninhar componentes, sua marcação pode ficar suja:

```html
<div class='search-form'>
  <input class='input' type='text'>
  <button class='search-button -red -large'></button>
</div>
```

Você pode simplificar isso usando o mecanismo de `@extend` do seu pré-processador:

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

E quanto a repetir elementos, como listas? Saiba mais sobre layouts.
[Continue →](layouts.md)
<!-- {p:.pull-box} -->
