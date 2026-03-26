# Noções básicas de HTML

## Objetivo da aula

Ao final desta aula, você vai conseguir:

- **Explicar o que é HTML** (e o papel dele na Web)
- Entender **quem define o padrão** (WHATWG vs W3C) e por que isso importa
- Entender o que as pessoas chamam de “HTML5” e a ideia de **living standard**
- **Criar e ler trechos simples de HTML** (parágrafo e lista)
- Separar a ideia de **estrutura (HTML)** vs **apresentação (CSS)**

---

## 1) HTML é um padrão (e alguém define as regras)

HTML é um padrão definido pelo **WHATWG** (*Web Hypertext Application Technology Working Group*), um grupo formado por pessoas que trabalham nos navegadores mais populares.

Ou seja: na prática, empresas como Google, Mozilla, Apple e Microsoft participam desse ecossistema.

- Site do WHATWG (pra descrição da aula): <https://whatwg.org/>

No passado, o **W3C** (*World Wide Web Consortium*) era o principal responsável pelo padrão HTML.

Esse “controle” migrou para o WHATWG quando ficou claro que a tentativa de empurrar o HTML para uma direção muito rígida (XHTML) não fazia sentido para a Web real.

---

## 2) O contexto: XHTML (por que quase mudou tudo)

Se você nunca ouviu falar de XHTML, aqui vai o resumo do que importa:

No começo dos anos 2000, muita gente acreditava que o futuro da Web seria o **XML**.  
Então tentaram transformar o HTML em uma linguagem de marcação “no estilo XML”, com mais regras e mais rigidez.

Só que isso colocava fricção demais no desenvolvimento do dia a dia.  
No fim, os fornecedores de navegadores perceberam que esse não era o caminho certo e recuaram - e o HTML seguiu evoluindo no caminho que a gente conhece.

---

## 3) “HTML5” e o que isso significa hoje

Eu mencionei “HTML5”. Vale entender a história porque isso aparece em vagas, em artigos e em conversas.

Tivemos o HTML 1 (1993). Aqui está o RFC original (bom link pra descrição da aula):

<https://tools.ietf.org/html/rfc1983>

Depois:

- HTML 2 em 1995
- HTML 3 em janeiro de 1997
- HTML 4 em dezembro de 1997

E depois de anos (com o episódio do XHTML no meio), chegou o termo “HTML5”.

Mas hoje a ideia principal é esta:

**Não existe “uma versão fechada” de HTML. É um padrão vivo (*living standard*).**

Isso é parecido com:

- **CSS**, que muita gente chama de “CSS3”, mas na prática são vários módulos.
- **JavaScript**, que tem edições anuais, mas o que manda é o suporte dos motores e navegadores.

Sim, a gente chama de HTML5 por hábito, mas o “HTML4” é de 1997 - tempo demais pra um mundo que muda tão rápido quanto a Web.

Aqui é onde a especificação do HTML “vive” hoje (bom link pra descrição):

<https://html.spec.whatwg.org/multipage>

---

## 4) O que é HTML, na prática

HTML é a linguagem de marcação que usamos para **estruturar conteúdo** na Web.

E existem várias maneiras desse HTML chegar no navegador:

- Um **servidor** pode gerar HTML (Rails, Laravel, Django…)
- Um app **JavaScript no cliente** pode gerar HTML em tempo real
- No caso mais simples, o HTML pode estar em um **arquivo `.html`** servido por um servidor web

Nesta fase do módulo, a gente vai mergulhar bastante nesse caso simples, porque ele mostra os blocos de construção sem distrações.

---

## 5) Tags, significado e exemplos simples

Por convenção, um arquivo HTML tem extensão `.html` (ou `.htm`).

Dentro desse arquivo, organizamos o conteúdo com **tags**.  
As tags agrupam o conteúdo e dão um significado para o texto.

Exemplo: um parágrafo com `p`:

```html
<p>Um parágrafo de texto</p>
```

Exemplo: uma lista não ordenada com `ul` e itens `li`:

```html
<ul>
  <li>Um item</li>
  <li>Outro item</li>
  <li>Mais um item</li>
</ul>
```

Quando o navegador exibe uma página HTML, ele interpreta as tags e renderiza os elementos com regras padrão (por exemplo, links azuis e sublinhados, listas com marcadores…).

Algumas regras são “do navegador”. Outras você define com CSS.

E aqui entra uma ideia central do módulo:

**HTML não é apresentação. HTML é significado/estrutura.**  
Quem cuida do “visual” é o CSS (e, quando necessário, o JavaScript).

---

## 6) Mini-exercício (2–3 minutos)

Crie um arquivo chamado `index.html` e escreva só isso:

```html
<p>Meu primeiro parágrafo</p>

<ul>
  <li>Aprender HTML</li>
  <li>Aprender CSS</li>
  <li>Aprender JavaScript</li>
</ul>
```

Agora abra esse arquivo no navegador e responda:

- O parágrafo aparece “simples”, e a lista aparece com bolinhas. **De onde vem esse visual?**
- Se HTML não é apresentação, qual é o papel do CSS nessa história?

---

## 7) Fechamento

- HTML é um **padrão** e ele “vive” hoje na especificação do WHATWG.
- O HTML passou por discussões históricas (W3C, XHTML), mas a Web priorizou pragmatismo.
- “HTML5” hoje é mais um termo popular: o importante é entender que o HTML é um **living standard**.
- HTML estrutura e dá significado; CSS cuida da aparência.
