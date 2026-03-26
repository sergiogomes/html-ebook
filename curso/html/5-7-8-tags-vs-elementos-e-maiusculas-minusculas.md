# Módulo HTML - Tags vs elementos, maiúsculas/minúsculas e espaço em branco (roteiro de aula)

## Objetivo da aula

Ao final desta aula, você vai conseguir:

- Explicar a diferença entre **tag** e **elemento**
- Saber se HTML diferencia **maiúsculas/minúsculas** (e qual padrão usar)
- Entender como o navegador trata **espaços em branco** no HTML
- Aplicar boas práticas de **legibilidade e consistência** no seu código

---

## 1) O que vamos esclarecer hoje

Nesta aula, vamos esclarecer três pontos que geram bastante dúvida no começo:

1. qual é a diferença entre tag e elemento;
2. se HTML diferencia letras maiúsculas e minúsculas;
3. como o navegador trata espaços em branco no HTML.

---

## 2) Tags vs elementos

Eu mencionei tags e elementos. Qual é a diferença?

Os elementos têm uma tag inicial e uma tag final. Neste exemplo, usamos as tags `p` de início e fechamento para criar um elemento `p`:

```html
<p>Um parágrafo de texto</p>
```

Assim, um elemento constitui todo o pacote:

- tag inicial;
- conteúdo de texto (e possivelmente outros elementos);
- tag de fechamento.

Se um elemento não tiver uma tag de fechamento, ele será escrito apenas com a tag de início e não poderá conter conteúdo de texto.

No dia a dia, é comum usar "tag" e "elemento" como sinônimos em conversas mais rápidas. Mas tecnicamente, essa é a diferença.

---

## 3) Diferença de maiúsculas e minúsculas

HTML não diferencia maiúsculas de minúsculas. Podemos escrever tags em letras maiúsculas ou minúsculas.

Nos primeiros dias da Web, maiúsculas eram comuns. Hoje, escrever em minúsculas virou o padrão de mercado por legibilidade e consistência.

A forma recomendada é esta:

```html
<p>Um parágrafo de texto</p>
```

E não esta:

```html
<P>Um parágrafo de texto</P>
```

Os dois exemplos funcionam, mas manter tudo em minúsculas deixa seu HTML mais limpo e mais fácil de manter ao longo do módulo.

---

## 4) Espaço em branco

Esse ponto é muito importante: em HTML, mesmo que você adicione vários espaços em branco em uma linha, o navegador normalmente colapsa esses espaços na renderização.

Por exemplo, a renderização deste parágrafo:

```html
<p>Um parágrafo de texto</p>
```

é a mesma que esta:

```html
<p> Um parágrafo de texto</p>
```

e também a mesma que esta:

```html
<p>Um parágrafo

de

        texto </p>
```

Com a propriedade CSS `white-space`, você pode alterar esse comportamento quando precisar.

A recomendação prática é: use a sintaxe que deixa o código mais organizado e fácil de ler.

Eu normalmente prefiro:

```html
<p>Um parágrafo de texto</p>
```

ou:

```html
<p>
  Um parágrafo de texto
</p>
```

Tags aninhadas devem ser indentadas com 2 ou 4 espaços (o mais importante é manter consistência):

```html
<body>
  <p>
    Um parágrafo de texto
  </p>
  <ul>
    <li>Um item de lista</li>
  </ul>
</body>
```

Se você quiser adicionar espaço visual entre elementos, prefira CSS em vez de tentar "forçar" com espaços no HTML. Exemplo:

```html
<p>
  Um parágrafo de texto <span style="margin: 0 10px;">e texto afastado</span>
</p>
```

Em casos excepcionais, você pode usar `&nbsp;` (espaço inquebrável), mas sem exagero. Para apresentação visual, CSS continua sendo a melhor opção. Para consultar outras entidades HTML, veja: <https://www.devmedia.com.br/html-entities-html-symbols-html-characters/1011>.

---

## 5) Mini-exercício (2 minutos)

Crie um arquivo HTML e escreva três versões do mesmo parágrafo (como nos exemplos da aula). Depois:

- Abra no navegador e confirme que o resultado visual é o mesmo.
- No seu editor, escolha uma formatação que fique mais legível pra você (uma linha vs várias linhas).

Perguntas rápidas:

- Quando você falaria “tag” e quando falaria “elemento”?
- Qual padrão você vai adotar no módulo: `<p>` ou `<P>`?

---

## 6) Fechamento (resumo curto)

- **Elemento** é o pacote completo (tag de abertura + conteúdo + tag de fechamento).
- HTML **não** diferencia maiúsculas/minúsculas, mas o padrão moderno é escrever tags em **minúsculas**.
- O navegador geralmente **colapsa espaços em branco**; use HTML organizado e deixe “espaçamento visual” para o CSS.
