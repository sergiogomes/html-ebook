# Noções básicas de HTML

HTML é um padrão definido pelo WHATWG, um acrônimo para Web Hypertext Application Technology Working Group, uma organização formada por pessoas que trabalham no navegador da web mais popular. O que significa que Google, Mozilla, Apple e Microsoft o controlam. No passado, o W3C (World Wide Web Consortium) era o responsável pela criação do padrão HTML. O controle mudou informalmente de W3C para WHATWG quando ficou claro que o avanço do W3C em direção ao XHTML não era uma boa ideia. Se você nunca ouviu falar de XHTML, aqui está uma pequena história. No início dos anos 2000, todos acreditávamos que o futuro da Web seria o XML. Assim, o HTML passou de uma linguagem de autoria baseada em SGML para uma linguagem de marcação XML. Foi uma mudança significativa.
Tínhamos que conhecer e respeitar mais regras. Por fim, os fornecedores de navegadores perceberam que esse não era o caminho certo para a Web e recuaram, criando o que hoje é conhecido como HTML5. O W3C discordou de desistir do controle do HTML e, durante anos, tivemos dois padrões concorrentes, cada um com o objetivo de ser o oficial. Finalmente, em 28 de maio de 2019, foi oficializado pelo W3C que a versão HTML "verdadeira" era a publicada pelo WHATWG. Eu mencionei HTML5. Deixe-me explicar esta pequena história. Não é aparente, como acontece com muitas coisas na vida quando muitos atores estão envolvidos, mas também é fascinante.
Tínhamos a versão 1 do HTML em 1993. Aqui está o RFC original: <https://tools.ietf.org/html/rfc1983>. O HTML 2 veio em 1995. Recebemos o HTML 3 em janeiro de 1997 e o HTML 4 em dezembro de 1997. Tempos ocupados! Mais de 20 anos se passaram, tínhamos toda essa coisa de XHTML e, eventualmente, chegamos a esse HTML5, que não é mais apenas HTML. HTML5 é um termo que agora define todo um conjunto de tecnologias, incluindo HTML, mas adicionando muitas APIs e padrões como WebGL, SVG e muito mais. A principal coisa a entender aqui é esta: não existe uma versão HTML agora. É um padrão de vida. Como o CSS, que é chamado de "3", mas na realidade é um monte de módulos independentes desenvolvidos separadamente. Como o JavaScript, onde temos uma nova edição a cada ano, mas hoje em dia, a única coisa que importa é qual mecanismo implementa recursos individuais. Sim, nós o chamamos de HTML5, mas o HTML4 é de 1997. É muito tempo para qualquer coisa, muito menos para a Web. Aqui é onde o padrão agora "vive": <https://html.spec.whatwg.org/multipage>. HTML é a linguagem de marcação que usamos para estruturar o conteúdo que consumimos na Web. Existem diferentes maneiras de fornecer HTML ao navegador.

- Um aplicativo do lado do servidor pode gerá-lo dependendo da solicitação ou dos dados da sessão, como um aplicativo Rails, Laravel ou Django.
- Um aplicativo JavaScript do lado do cliente pode gerar o HTML em tempo real.
- No caso mais simples, pode ser armazenado em um arquivo e enviado ao navegador por um servidor Web.

Vamos mergulhar neste último caso. Embora seja provavelmente a forma menos popular de gerar HTML na prática, ainda é essencial conhecer os blocos de construção básicos. Por convenção, um arquivo HTML tem uma extensão .html ou .htm. Dentro desse arquivo, organizamos o conteúdo por meio de tags. As tags agrupam o conteúdo e cada tag dá um significado especial ao texto que envolve. Vamos dar alguns exemplos.
Este trecho de HTML cria um parágrafo usando a tag p:

```html
<p>Um parágrafo de texto</p>
```

Este trecho de HTML cria uma lista de itens usando a tag ul, que significa lista não ordenada, e as tags li, que significa item de lista:

```html
<ul>
   <li>Primeiro item</li>
   <li>Segundo item</li>
   <li>Terceiro item</li>
</ul>
```

Quando o navegador exibe uma página HTML, ele interpreta as tags e renderiza os elementos de acordo com as regras que definem sua aparência visual. Algumas regras são integradas, como como uma lista é renderizada ou um link é sublinhado em azul. Você define algumas outras regras com CSS. HTML não é de apresentação. Não está preocupado com a aparência das coisas. Em vez disso, está preocupado com o que as coisas significam. Cabe ao navegador determinar como as coisas ficarão, com as diretrizes definidas por quem constrói a página com a linguagem CSS. Esses dois exemplos que fiz são trechos de HTML obtidos fora do contexto de uma página.
