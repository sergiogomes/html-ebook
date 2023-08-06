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

## As tags de título

O HTML nos fornece 6 tags de título. Do mais importante para o menos importante, temos `h1`, `h2`, `h3`, `h4`, `h5` e `h6`.
Normalmente, uma página terá um elemento `h1`, o título da página. Então você tem um ou mais elementos `h2` dependendo do conteúdo da página.
Os cabeçalhos, especialmente a organização do título, também são essenciais para o SEO, e os mecanismos de pesquisa os utilizam de várias maneiras.
O navegador renderizará a tag `h1` maior e diminuirá o tamanho dos elementos à medida que o número próximo a `h` aumenta por padrão

```html
<h1>h1</h1>
<h2>h2</h2>
<h3>h3</h3>
<h4>h4</h4>
<h5>h5</h5>
<h6>h6</h6>
<p>p</p>
```

Todos os cabeçalhos são elementos de bloco. Eles não podem conter outros elementos, apenas texto.

## A tag strong

Usamos a tag `strong` para marcar o texto dentro dela como forte, o que é essencial, pois não é uma dica visual, mas sim semântica. Dependendo do meio utilizado, sua interpretação irá variar.
Os navegadores tornam o texto nesta tag `negrito` por padrão.

```html
<p>Este parágrafo é muito <strong>importante!</strong></p>
```

## A tag em

Usamos a tag `em` para marcar o texto dentro dela como enfatizado. Como strong, não é um visual, mas uma dica semântica. Navegadores fazem o texto `itálico` por padrão.

```html
<p><em>Status quo</em> é uma frase em Latim que significa o estado de coisas existente</p>
```

## Citações

A tag `blockquote` ajuda a inserir citações no texto.
Os navegadores aplicam uma margem ao elemento `blockquote` por padrão (o Chrome aplica uma margem esquerda e direita de 40px e uma margem superior e inferior de 10px)

```html
<blockquote>
  A maioria das pessoas gasta mais tempo e energia contornando os problemas do que tentando resolvê-los.<br>
  - Henry Ford
</blockquote>
```

E usamos a tag `q` para citações em linha.

```html
<p>Henry Ford disse <q>A maioria das pessoas gasta mais tempo e energia contornando problemas do que tentando resolvê-los.</q> no século 20</p>
```
