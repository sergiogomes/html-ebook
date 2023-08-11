# Tags de Contêiner

O HTML fornece um conjunto de tags de contêiner. Essas tags podem conter um grupo não especificado de outras tags.
Nós temos:

- article
- section
- div

É preciso esclarecer para entender a diferença entre eles. Vamos ver quando usar cada um.

## article

A tag `article` identifica uma coisa que pode ser independente de outras coisas em uma página.
Por exemplo, uma lista de postagens de blog na página inicial.
Ou uma lista de links.

```html
<div>
  <article>
    <h2>Uma postagem no blog</h2>
    <a ...>Leia mais</a>
  </article>
  <article>
    <h2>Outra postagem no blog</h2>
    <a ...>Leia mais</a>
  </article>
</div>
```

Não estamos limitados a listas: um `article` pode ser o elemento principal de uma página.

```html
<article>
  <h2>Uma postagem no blog</h2>
  <p>Aqui está o conteúdo...</p>
</article>
```

Dentro de uma tag de article, devemos ter um título ( `h1` - `h6` )

## section

A tag `section` representa uma seção de um documento. Cada `section` tem uma tag de cabeçalho ( `h1` - `h6` ), então o corpo da seção.
Exemplo:

```html
<section>
   <h2>Uma seção da página</h2>
   <p>...</p>
   <img...>
</section>
```

É útil dividir um artigo longo em diferentes seções.
Não devemos usá-lo como um elemento contêiner genérico porque temos a tag `div`.

## div

A tag `div` é o elemento contêiner genérico:

```html
<div>
  ...
</div>
```

Muitas vezes adicionamos um atributo `class` ou `id` a este elemento para adicionar estilos a ele usando CSS.
Usamos `div` em qualquer lugar onde precisamos de um contêiner e as tags existentes não são adequadas.
