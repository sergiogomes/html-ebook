# Tags de página

## nav

Podemos usar a tag `nav` para criar a marcação de navegação da página. Dentro dela, normalmente adicionamos uma lista `ul` ou `ol`:

```html
<nav>
  <ol>
    <li><a href="/">Página inicial</a></li>
    <li><a href="/blog">Blog</a></li>
  </ol>
</nav>
```

## aside

Podemos usar a tag `aside` para adicionar conteúdo extra relacionado ao conteúdo principal.
Uma caixa onde adicionar uma citação, por exemplo. Ou uma barra lateral.
Exemplo:

```html
<div>
  <p>algum texto..</p>
  <aside>
    <p>Uma citação..</p>
  </aside>
  <p>outro texto...</p>
</div>
```

Usar `aside` sinaliza que as coisas que ele contém não fazem parte do fluxo regular da seção que ele vive.

## header

Podemos usar a tag `header` para representar uma parte da página que é a introdução. Ele pode, por exemplo, conter uma ou mais tags de título ( `h1` - `h6` ), o slogan do artigo e uma imagem.

```html
<body>
  <header>
    <h1>Título do artigo</h1>
  </header>
  ...
</body>
```

## main

Podemos usar a tag `main` para representar a parte principal de uma página:

```html
<body>
  ....
  <main>
    <p>....</p>
  </main>
  ...
</body>
```

## footer

Podemos usar a tag `footer` para determinar o rodapé de um artigo ou o rodapé da página:

```html
<article>
  ....
  <footer>
    <p>Notas de rodapé..</p>
  </footer>
</article>
```
