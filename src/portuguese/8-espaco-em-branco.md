# Espaço em Branco

Muito importante. Em HTML, mesmo que você adicione vários espaços em branco em uma linha, ela é recolhida pelo mecanismo CSS do navegador.
Por exemplo, a renderização deste parágrafo:

```html
<p>Um parágrafo de texto</p>
```

É o mesmo que isto:

```html
<p> Um parágrafo de texto</p>
```

E o mesmo que isto:

```html
<p>Um parágrafo

de

        texto </p>
```

Usando a propriedade CSS de espaço em branco, você pode alterar o comportamento das coisas. Você pode encontrar mais informações sobre como o CSS processa o espaço em branco no CSS Spec.

Use a sintaxe que torna as coisas visualmente mais organizadas e fáceis de ler, mas você pode usar qualquer sintaxe que desejar.
Eu normalmente prefiro

```html
<p>Um parágrafo de texto</p>
```

ou

```html
<p>
  Um parágrafo de texto
</p>
```

Tags aninhadas devem ser indentadas com 2 ou 4 caracteres, dependendo de sua preferência:

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

> Observação: esse recurso "espaço em branco não é relevante" significa que, se você quiser adicionar espaço adicional, isso pode deixá-lo furioso. Sugiro que você use CSS para criar mais espaço quando necessário.

---

> Observação: em casos excepcionais, você pode usar o &nbsp; Entidade HTML (um acrônimo que significa espaço ininterrupto) - mais sobre entidades HTML posteriormente. Porém, não devemos usá-lo em excesso. CSS é sempre preferido para alterar a apresentação visual.
