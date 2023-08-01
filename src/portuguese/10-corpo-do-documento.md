# O corpo do documento

Depois da tag head de fechamento, só podemos ter uma coisa em um documento HTML: o elemento `body`.

```html
<!DOCTYPE html>
<html>
  <head>
    ...
  </head>
  <body>
    ...
  </body>
</html>
```

Assim como as tags head e html, só podemos ter uma tag body na página.
Todas as tags que definem o conteúdo da página estão dentro da tag body.
Tecnicamente, as tags de início e fim são opcionais. Mas é uma boa prática adicioná-los.
Nos capítulos seguintes, definiremos as várias tags que você pode usar dentro do corpo da página.
Mas antes, devemos introduzir uma diferença entre elementos de bloco e elementos em linha.

## Elementos Block vs. Elementos Inline

Os elementos visuais, aqueles definidos no corpo da página, geralmente podem ser classificados em duas categorias:

- elementos de bloco (p, div, elementos de cabeçalho, listas, itens de lista, etc...)
- elementos em linha (a, span, img, etc...)

Qual é a diferença?
Quando posicionados na página, os elementos de bloco não permitem outros elementos próximos a eles, à esquerda ou à direita.
Em vez disso, os elementos em linha podem ficar ao lado de outros elementos em linha.
A diferença também está nas propriedades visuais que podemos editar usando CSS. Nos elementos de bloco podemos alterar `width`/`height`, `margin`, `padding` e `border`. Não podemos fazer isso para elementos em linha.

> Observe que usando CSS, podemos alterar o padrão de cada elemento, definindo uma tag p para ser em linha, por exemplo, ou um span para ser um elemento de bloco.

Outra diferença é que os elementos de bloco podem conter elementos em linha. O inverso não é válido.
Alguns elementos de bloco podem conter outros elementos de bloco, mas isso depende. A tag `p`, por exemplo, não permite isso.
