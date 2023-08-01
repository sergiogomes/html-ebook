# Tags que interagem com o texto

## A tag p

Esta tag define um parágrafo de texto.

```html
<p>Algum texto</p>
```

É um elemento de bloco.
Dentro dela, podemos adicionar qualquer elemento em linha, como `span` ou `a`. Não podemos adicionar elementos de bloco.
Não podemos aninhar um elemento `p` em outro.
Os navegadores estilizam um parágrafo com uma margem na parte superior e inferior por padrão (16px no Chrome, mas o valor exato pode variar entre os navegadores). A margem causa espaço entre dois parágrafos consecutivos, replicando o que pensamos ser um "parágrafo" em um texto impresso.

## A tag span

O `span` é uma tag em linha usada para criar uma seção em um parágrafo que podemos segmentar usando CSS:

```html
<p>Uma parte do texto <span>e aqui outra parte</span></p>
```

## A tag br

A tag `br` representa uma quebra de linha. É um elemento em linha e não
precisa de uma etiqueta de fechamento.
Nós o usamos para criar uma nova linha dentro de uma tag `p` sem criar um novo parágrafo. E em comparação com a criação de um novo parágrafo, não adiciona espaçamento adicional.

```html
<p>Algum texto<br>Uma nova linha</p>
```
