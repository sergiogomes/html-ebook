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

## Imagens responsivas usando srcset

Com o atributo `srcset`, podemos definir imagens responsivas que o navegador pode usar dependendo da densidade de pixels ou largura da janela, de acordo com suas preferências. Dessa forma, ele só poderá baixar os recursos necessários para renderizar a página, sem baixar uma imagem maior se estiver em um dispositivo móvel, por exemplo.
Aqui está um exemplo onde fornecemos quatro imagens adicionais para quatro tamanhos de tela diferentes:

```html
<img
  src="cachorro.png"
  alt="A foto de um cachorro."
  srcset="
    cachorro-500.png 500w,
    cachorro-800.png 800w,
    cachorro-1000.png 1000w,
    cachorro-1400.png 1400w
  "
>
```

No `srcset`, usamos a medida `w` para indicar a largura da janela. Para isso, também precisamos usar o atributo `sizes`:

```html
<img
  src="cachorro.png"
  alt="A foto de um cachorro."
  sizes="(max-width: 500px) 100vw, (max-width: 900px) 50vw, 800px"
  srcset="
    cachorro-500.png 500w,
    cachorro-800.png 800w,
    cachorro-1000.png 1000w,
    cachorro-1400.png 1400w
  "
>
```

Neste exemplo, a string `(max-width: 500px) 100vw, (max-width: 900px) 50vw, 800px` no atributo tamanhos descreve o tamanho da imagem em comparação com a janela de visualização, com múltiplas condições separadas por ponto e vírgula.
A condição de mídia `max-width: 500px` define o tamanho da imagem em correlação com a largura da janela de visualização. Resumindo, se o tamanho da janela for `< 500px`, a imagem será renderizada em 100% do tamanho da janela.
Se o tamanho da janela for grande, mas `< 900px`, a imagem será renderizada em 50% do tamanho da janela.
E se for ainda maior, renderiza a imagem em 800px.
A unidade de medida `vw` pode ser nova para você e, resumindo, um `vw` é 1% da largura da janela, então `100vw` é 100% da largura da janela.
Um site útil para gerar o `srcset` e imagens progressivamente menores é <https://responsivebreakpoints.com/>.
