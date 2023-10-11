# Imagens

As imagens podem ser exibidas usando a tag `img`.
Esta tag aceita um atributo src, que usamos para definir a fonte da imagem:

```html
<img src="imagem.png">
```

Podemos usar um amplo conjunto de imagens. Os mais comuns são PNG, JPEG, GIF, SVG e, mais recentemente, WebP.
O padrão HTML requer a presença de um atributo `alt` para descrever a imagem. É usado por leitores de tela e também por bots de mecanismos de pesquisa:

```html
<img src="cachorro.png" alt="A foto de um cachorro">
```

Você pode definir os atributos `width` e `height` para definir o espaço que o elemento ocupará para que o navegador possa considerá-lo e não alterar o layout quando a imagem estiver totalmente carregada. Leva um valor numérico expresso em pixels.

```html
<img src="cachorro.png" alt="A foto de um cachorro" width="300" height="200">
```

## A tag da figura

Muitas vezes podemos usar a tag `figure` junto com a tag `img`.
`figure` é uma tag semântica frequentemente usada quando você deseja exibir uma imagem com uma legenda. Você usa assim:

```html
<figure>
  <img src="cachorro.png" alt="Um lindo cachorro">
  <figcaption>Um lindo cachorro</figcaption>
</figure>
```

A tag `figcaption` envolve o texto da legenda.
