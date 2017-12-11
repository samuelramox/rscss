# Armadilhas

## Herança através de componentes aninhados
Tenha cuidado com os componentes aninhados com elementos que compartilham o mesmo nome que os elementos em seu container.

```html
<article class='article-link'>
 <div class='vote-box'>
    <button class='up'></button>
    <button class='down'></button>
    <span class='count'>4</span>
  </div>

  <h3 class='title'>Article title</h3>
  <p class='count'>3 votes</p>
</article>
```

```scss
.article-link {
  > .title { /* ... */ }
  > .count { /* ... (!!!) */ }
}

.vote-box {
  > .up { /* ... */ }
  > .down { /* ... */ }
  > .count { /* ... */ }
}
```

Nesse caso, se `.article-link > .count` não tiver o seletor `>` (filho), ele também será aplicado ao elemento `.vote-box .count`. Esta é uma das razões pelas quais os seletores filho são preferidos.
