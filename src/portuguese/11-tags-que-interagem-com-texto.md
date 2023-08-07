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

A tag `br` representa uma quebra de linha. É um elemento em linha e não precisa de uma tag de fechamento.
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

## Linha horizontal

Não é realmente baseado em texto, mas podemos usar a tag `hr` dentro de uma página. Significa régua horizontal e adiciona uma linha horizontal à página.
Útil para separar seções na página.

```html
<hr>
```

## Blocos de código

A tag `code` é especialmente útil para mostrar o código porque os navegadores fornecem uma fonte monoespaçada.
Normalmente, essa é a única coisa que os navegadores fazem. Aqui está o CSS aplicado pelo Chrome:

```css
code {
  font-family: monospace;
}
```

Essa tag normalmente é agrupada em uma tag `pre` porque a tag code ignora espaços em branco e quebras de linha como a tag `p`.
O Chrome aplica esse estilo padrão à `pre` para evitar que o espaço em branco colapse e o torne um elemento de bloco.

```css
pre {
  display: block;
  font-family: monospace;
  white-space: pre;
  margin: 1em 0px;
}
```

## Listas

Temos três tipos de listas:

- listas não ordenadas
- listas ordenadas
- listas de definição

Criamos listas não ordenadas usando a tag `ul`. Cada item na lista com a tag `li`:

```html
<ul>
  <li>ovos</li>
  <li>bacon</li>
</ul>
```

As listas ordenadas são semelhantes, apenas feitas com a tag `ol`:

```html
<ol>
  <li>Primeiro</li>
  <li>Segundo</li>
</ol>
```

A diferença é que as listas ordenadas possuem um número antes de cada item.
As listas de definições são diferentes. Você tem um termo e sua definição:

```html
<dl>
  <dt>Sérgio</dt>
  <dd>O nome</dd>
  <dt>Gomes</dt>
  <dd>O sobrenome</dd>
</dl>
```

Você raramente os vê por aí, com certeza não muito como `ul` e `ol`, mas às vezes eles podem ser úteis.

## Outras tags de texto

Existem várias tags com propósitos de apresentação:

- a tag mark
- a tag ins
- a tag del
- a tag sup
- a tag sub
- a tag small
- a tag i
- a tag b

Aqui está um exemplo da renderização visual deles, que é aplicada por padrão pelos navegadores:

```html
<mark>mark</mark>
<ins>ins</ins>
<del>del</del>
<sup>sup</sup>
<sub>sub</sub>
<small>small</small>
<i>i</i>
<b>b</b>
```

Você pode se perguntar, como `b` é diferente de `strong`? E como `i` é diferente de `em`?
A diferença está no significado semântico. Enquanto `b` e `i` são uma dica direta no navegador para tornar um texto em negrito ou itálico, `strong` e `em` dão ao texto um significado especial. Cabe ao navegador fornecer o estilo, que é o mesmo que `b` e `i`, por padrão. Embora você possa mudar isso usando CSS.

Existem muitas outras tags menos usadas relacionadas ao texto. Eu apenas mencionei as que eu vejo mais sendo usadas.
