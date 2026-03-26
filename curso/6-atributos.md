# Módulo HTML — Atributos (roteiro de aula)

## Objetivo da aula

Ao final desta aula, você vai conseguir:

- **Explicar o que são atributos** e por que eles existem no HTML
- **Ler e escrever atributos** com a sintaxe correta
- **Entender atributos booleanos**
- **Usar `class` e `id` com segurança**, sabendo quando cada um faz sentido
- **Reconhecer atributos comuns** e quando eles são específicos de uma tag

> Este documento serve como **descrição e suporte da aula**: você pode ler como roteiro e também usar como referência depois.

---

## 1) O que são atributos (ideia principal)

Quando você escreve um elemento HTML, a **tag de abertura** pode carregar informações extras.  
Essas informações extras são os **atributos**.

Pensa assim: o elemento é “o que é”, e o atributo é “alguma característica ou configuração” daquele elemento.

- O elemento `<p>` diz “isso é um parágrafo”.
- Um atributo como `class="intro"` pode dizer “esse parágrafo pertence ao grupo *intro*”.
- Um atributo como `id="topo"` pode dizer “esse parágrafo tem um identificador único”.

---

## 2) Sintaxe dos atributos (como escrever)

A forma mais comum é **chave e valor**:

- **`key="value"`**

Exemplo:

```html
<p class="a-class">Um parágrafo de texto</p>
```

Você também pode usar **aspas simples**, mas em HTML o mais comum é manter **aspas duplas** como convenção.

Você pode ter **vários atributos** no mesmo elemento:

```html
<p class="a-class" id="an-id">Um parágrafo de texto</p>
```

---

## 3) Atributos booleanos (quando não tem valor)

Alguns atributos são chamados de **booleanos**.  
Isso significa que o simples fato do atributo existir já indica “ligado / verdadeiro”.

Um exemplo bem comum:

```html
<script defer src="file.js"></script>
```

Aqui, `defer` é booleano: se ele está presente, o navegador aplica o comportamento do `defer`.

> Observação prática: existem dois “tipos” que você vai ver bastante no dia a dia:
>
> - **Atributos com valor** (`src="..."`, `href="..."`, `class="..."`)
> - **Atributos booleanos** (`defer`, `disabled`, `checked`, `required`, etc.)

---

## 4) `id` vs `class` (muito importante)

Os atributos **`class` e `id`** são os mais comuns, porque eles são úteis tanto em **CSS** quanto em **JavaScript**.

### `id` — único na página

Um `id` deve ser **único** dentro da página (dentro do documento HTML).  
Ou seja, você **não** deve repetir o mesmo `id` em dois elementos diferentes.

Exemplo:

```html
<h1 id="titulo-principal">Bem-vindo</h1>
```

Uso típico de `id`:

- **Âncoras** (navegar para uma parte da página)
- **Referência única** em scripts (quando realmente faz sentido ser único)

### `class` — pode repetir (e é o mais comum no CSS)

Já a `class` pode aparecer **várias vezes**, em vários elementos.  
Isso é ótimo para criar “grupos” de elementos com o mesmo estilo ou comportamento.

Exemplo:

```html
<p class="aviso">Atenção: leia isso!</p>
<p class="aviso">Atenção: isso também!</p>
```

E uma classe pode ter **vários valores**, separados por espaço:

```html
<p class="a-class another-class">Um parágrafo de texto</p>
```

Na prática, isso significa: o elemento pertence às classes `a-class` **e** `another-class`.

### Convenção de nomes de classes

É comum usar **traço `-`** para separar palavras:

- `menu-principal`
- `btn-primario`
- `card-produto`

Não é regra do HTML — é **convenção** para facilitar leitura e padronização.

---

## 5) Atributos comuns do dia a dia (mapa mental rápido)

Além de `class` e `id`, alguns atributos aparecem muito:

- **`href`**: links (`<a href="...">`)
- **`src`**: fontes de mídia/arquivos (`<img src="...">`, `<script src="...">`)
- **`alt`**: texto alternativo de imagem (`<img alt="...">`)
- **`title`**: título/tooltip (várias tags)
- **`style`**: CSS inline (funciona, mas use com cuidado)

E também existem atributos **bem específicos** de determinadas tags. Exemplo:

- `type` em `<input>`
- `placeholder` em `<input>`
- `rel` e `target` em `<a>`

---

## 6) `style` (CSS inline) — quando aparece e por que ter cuidado

Você pode usar `style` para colocar CSS **direto no elemento**:

```html
<p style="color: red; font-weight: bold;">
  Texto com estilo inline
</p>
```

Isso é útil para testes rápidos e exemplos, mas em projetos reais a regra geral é:

- **Preferir CSS em arquivos/estilos separados** (mais organização e reaproveitamento)
- Usar `style` só quando houver um motivo claro (ex.: protótipo, e-mails HTML, casos específicos)

---

## 7) Mini-exercício (2 minutos)

Crie um arquivo HTML simples e escreva:

1) Um título com `id="topo"`  
2) Dois parágrafos com a mesma classe `class="texto"`  
3) Um parágrafo com duas classes `class="texto destaque"`  
4) Um script com `defer` e `src`

Modelo (você pode copiar e adaptar):

```html
<h1 id="topo">Minha página</h1>

<p class="texto">Primeiro parágrafo</p>
<p class="texto">Segundo parágrafo</p>
<p class="texto destaque">Terceiro parágrafo com destaque</p>

<script defer src="app.js"></script>
```

Se você quiser checar entendimento, responda:

- **Quantos elementos podem ter o mesmo `id`?**  
- **Quantos elementos podem ter a mesma `class`?**
