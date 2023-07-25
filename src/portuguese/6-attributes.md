# Atributos

A tag inicial de um elemento pode ter trechos específicos de informações que podemos anexar, chamados de atributos.
Os atributos têm a sintaxe key="value":

```html
<p class="a-class">Um parágrafo de texto</p>
```

Você também pode usar aspas simples, mas usar aspas duplas em HTML é uma convenção excelente.
Podemos ter muitos deles:

```html
<p class="a-class" id="an-id">Um parágrafo de texto</p>
```

E alguns atributos são booleanos, o que significa que você só precisa da chave:

```html
<script defer src="file.js"></script>
```

Os atributos class e id são os mais comuns que você encontrará usados.
Eles têm um significado especial e são úteis tanto em CSS quanto em JavaScript.
A diferença entre os dois é que um id é único no contexto de uma página web; não podemos duplicá-lo.
Por outro lado, as classes podem aparecer várias vezes em vários elementos. Além disso, um id é apenas um valor. Uma classe pode conter vários valores separados por um espaço:

```html
<p class="a-class another-class">Um parágrafo de texto</p>
```

É comum usar o traço - para separar palavras em um valor de classe, mas é apenas uma convenção.
Esses são apenas dois dos possíveis atributos que você pode ter. Alguns atributos são usados apenas para uma tag e são altamente especializados.
Você acabou de ver id e class, mas temos outros, como style. Podemos usar o estilo para inserir regras CSS inline em um elemento.
