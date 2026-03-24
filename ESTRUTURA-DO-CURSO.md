# Estrutura do Curso de HTML

## Visão Geral

Curso completo de HTML para iniciantes, cobrindo desde os conceitos fundamentais até tópicos avançados.

---

## PARTE 1: Fundamentos

### Introdução

- Bem-vindo ao curso
- O que é HTML
- História do HTML
- Por que aprender HTML

### Prefácio

- HTML como base da Web
- Simplicidade e poder do HTML
- Compatibilidade com versões anteriores

### Capítulo 1 - Noções Básicas de HTML

- O que é HTML
- WHATWG vs W3C
- História: HTML 1, 2, 3, 4, XHTML e HTML5
- HTML como padrão vivo
- Como o HTML é fornecido ao navegador
- Extensões de arquivo (.html, .htm)
- Tags e seu significado
- Exemplos básicos (parágrafos, listas)
- HTML vs CSS (estrutura vs apresentação)

### Capítulo 2 - Estrutura da Página HTML

- A declaração DOCTYPE (`<!DOCTYPE html>`)
- O elemento `<html>`
- Tags de abertura e fechamento
- Tags auto-fechantes
- A estrutura básica: `<head>` e `<body>`
- Exemplo completo de estrutura

### Capítulo 3 - Tags vs Elementos

- Diferença entre tags e elementos
- Tag inicial, conteúdo e tag final
- Elementos sem tag de fechamento
- Uso dos termos no curso

### Capítulo 4 - Atributos

- O que são atributos
- Sintaxe: `key="value"`
- Aspas simples vs duplas
- Múltiplos atributos
- Atributos booleanos
- Atributos `class` e `id`
- Diferença entre `id` e `class`
- Múltiplas classes
- Convenções de nomenclatura
- Atributo `style` (CSS inline)

### Capítulo 5 - Diferença de Maiúsculas e Minúsculas

- HTML é case-insensitive
- Convenção: usar minúsculas
- Exemplos de uso correto

### Capítulo 6 - Espaço em Branco

- Como o HTML trata espaços em branco
- Múltiplos espaços são colapsados
- Quebras de linha são ignoradas
- Uso de CSS para controlar espaçamento
- Indentação recomendada (2 ou 4 espaços)
- A entidade `&nbsp;` (uso limitado)

---

## PARTE 2: Estrutura do Documento

### Capítulo 7 - O Cabeçalho do Documento (`<head>`)

- O que é a tag `<head>`
- Posicionamento no documento
- Tags que podem estar no `<head>`

#### A Tag `<title>`

- Definição do título da página
- Exibição no navegador
- Importância para SEO

#### A Tag `<script>`

- Adicionar JavaScript à página
- JavaScript inline
- Carregar arquivo JavaScript externo
- O atributo `src`
- O atributo `type` (opcional)
- Posicionamento: `head` vs `body`
- O atributo `defer`
- Performance e boas práticas

#### A Tag `<noscript>`

- Detectar quando scripts estão desabilitados
- Uso no `<head>` (tags permitidas)
- Uso no `<body>` (conteúdo)

#### A Tag `<link>`

- Relacionamentos entre documentos
- Vincular arquivo CSS externo
- O atributo `rel="stylesheet"`
- O atributo `media` (screen, print)
- Outros usos: RSS feeds, favicons
- `rel="prev"` e `rel="next"` (deprecated pelo Google)

#### A Tag `<style>`

- CSS inline no documento
- O atributo `media`

#### A Tag `<base>`

- Definir URL base para links relativos
- Quando usar

#### A Meta Tag (`<meta>`)

- Meta tags e SEO
- Meta tag de descrição
- Meta tag `charset` (UTF-8)
- Meta tag `robots` (noindex, nofollow)
- Meta tag `googlebot`
- Meta tag `notranslate`
- Meta tag `viewport` (responsividade)
- Meta tag `http-equiv="refresh"` (redirecionamento)

---

### Capítulo 8 - O Corpo do Documento (`<body>`)

- A tag `<body>`
- Posicionamento no documento
- Tags de início e fim (opcionais, mas recomendadas)
- Conteúdo da página

#### Elementos de Bloco vs. Elementos em Linha

- Diferença fundamental
- Elementos de bloco: não permitem elementos ao lado
- Elementos em linha: podem ficar lado a lado
- Propriedades CSS diferentes
- Elementos de bloco podem conter elementos em linha
- O inverso não é válido
- Alguns elementos de bloco podem conter outros elementos de bloco
- Mudança de comportamento com CSS

---

## PARTE 3: Conteúdo e Formatação de Texto

### Capítulo 9 - Tags que Interagem com o Texto

#### A Tag `<p>`

- Parágrafos de texto
- Elemento de bloco
- Conteúdo permitido (elementos em linha)
- Não pode aninhar outro `<p>`
- Margens padrão do navegador

#### A Tag `<span>`

- Elemento em linha genérico
- Uso para segmentação com CSS
- Exemplos práticos

#### A Tag `<br>`

- Quebra de linha
- Elemento em linha auto-fechante
- Diferença de criar novo parágrafo
- Quando usar

#### As Tags de Título (`<h1>` a `<h6>`)

- Hierarquia de títulos
- Importância do `<h1>`
- Estrutura recomendada
- Importância para SEO
- Renderização padrão (tamanhos)
- Elementos de bloco
- Conteúdo permitido (apenas texto)

#### A Tag `<strong>`

- Texto importante (semântico)
- Diferente de `<b>`
- Renderização padrão (negrito)
- Variação por meio de exibição

#### A Tag `<em>`

- Texto enfatizado (semântico)
- Diferente de `<i>`
- Renderização padrão (itálico)

#### Citações

- Tag `<blockquote>` (citações em bloco)
- Margens padrão
- Tag `<q>` (citações em linha)
- Quando usar cada uma

#### Linha Horizontal (`<hr>`)

- Separador visual
- Uso para separar seções
- Tag auto-fechante

#### Blocos de Código

- Tag `<code>` (trecho de código)
- Fonte monoespaçada
- Tag `<pre>` (bloco de código)
- Preservação de espaços em branco
- Uso combinado (`<pre><code>`)

#### Listas

- Listas não ordenadas (`<ul>` e `<li>`)
- Listas ordenadas (`<ol>` e `<li>`)
- Listas de definição (`<dl>`, `<dt>`, `<dd>`)
- Quando usar cada tipo

#### Outras Tags de Texto

- `<mark>` - Texto marcado
- `<ins>` - Texto inserido
- `<del>` - Texto deletado
- `<sup>` - Sobrescrito
- `<sub>` - Subscrito
- `<small>` - Texto pequeno
- `<i>` - Itálico (apresentação)
- `<b>` - Negrito (apresentação)
- Diferença semântica: `<strong>` vs `<b>`, `<em>` vs `<i>`

---

### Capítulo 10 - Links

#### Links Básicos

- A tag `<a>`
- O atributo `href`
- URLs absolutos
- URLs relativos
- Diferença entre `/sobre` e `sobre`
- Conteúdo do link (texto, imagens, outros elementos)
- Não pode aninhar outra tag `<a>`

#### Abrindo Links em Nova Aba

- O atributo `target="_blank"`
- Segurança: `rel="noopener noreferrer"`
- Por que usar `noopener`
- Exemplo completo e seguro

#### Links de Email

- `href="mailto:email@exemplo.com"`
- Assunto e corpo do email
- Múltiplos destinatários

#### Links de Telefone

- `href="tel:+5511999999999"`
- Formato internacional
- Uso em dispositivos móveis

#### Âncoras Internas

- Links para seções da mesma página
- `href="#secao"`
- Criando âncoras com `id`
- Navegação suave
- Links para outras páginas com âncoras

#### Download de Arquivos

- O atributo `download`
- Forçar download ao invés de navegar
- Nome do arquivo baixado

#### Atributos `rel`

- `rel="noopener"` - Segurança com `target="_blank"`
- `rel="noreferrer"` - Não enviar referrer
- `rel="nofollow"` - Não seguir link (SEO)
- `rel="external"` - Link externo
- `rel="prev"` e `rel="next"` - Navegação entre páginas

---

### Capítulo 11 - Imagens

#### A Tag `<img>`

- O atributo `src`
- Formatos de imagem suportados (PNG, JPEG, GIF, SVG, WebP)
- O atributo `alt` (obrigatório)
- Importância para acessibilidade e SEO
- Atributos `width` e `height`
- Prevenção de layout shift

#### A Tag `<figure>`

- Tag semântica para imagens
- Uso com `<img>`
- A tag `<figcaption>`
- Legendas de imagens

#### Imagens Responsivas

- O atributo `srcset`
- Diferentes tamanhos de imagem
- O atributo `sizes`
- Media queries em `sizes`
- Unidade `vw` (viewport width)
- Ferramentas para gerar `srcset`

---

## PARTE 4: Estruturação Avançada

### Capítulo 12 - Tags de Contêiner

#### A Tag `<div>`

- Elemento contêiner genérico
- Uso com `class` e `id`
- Quando usar `<div>`

#### A Tag `<section>`

- Seção de documento
- Requer título (`<h1>` a `<h6>`)
- Quando usar `<section>`
- Não usar como contêiner genérico

#### A Tag `<article>`

- Conteúdo independente
- Pode ser usado sozinho ou em lista
- Requer título (`<h1>` a `<h6>`)
- Exemplos: postagens de blog, notícias

---

### Capítulo 13 - Tags Semânticas HTML5 (Tags de Página)

#### A Tag `<nav>`

- Navegação da página
- Uso com listas (`<ul>` ou `<ol>`)
- Links de navegação

#### A Tag `<aside>`

- Conteúdo relacionado mas secundário
- Barras laterais
- Citações
- Não faz parte do fluxo principal

#### A Tag `<header>`

- Cabeçalho/introdução
- Pode conter títulos, slogans, imagens
- Pode ser usado em `<body>` ou dentro de `<article>`

#### A Tag `<main>`

- Conteúdo principal da página
- Deve haver apenas um por página
- Não deve estar dentro de `<article>`, `<aside>`, `<footer>`, `<header>` ou `<nav>`

#### A Tag `<footer>`

- Rodapé de artigo ou página
- Informações de contato, copyright, etc.
- Pode ser usado em `<body>` ou dentro de `<article>`

---

## PARTE 5: Formulários

### Capítulo 14 - Introdução aos Formulários

- O que são formulários
- Interação com páginas web
- A tag `<form>`
- Método GET (padrão)
- Método POST
- O atributo `method`
- O atributo `action`
- Envio de dados ao servidor
- Recarregamento da página (padrão)
- Controle com JavaScript (`event.preventDefault()`)
- Controles disponíveis (visão geral)

---

### Capítulo 15 - Inputs de Formulário

#### A Tag `<input>` - Visão Geral

- Elemento versátil
- Comportamento muda com `type`
- Tipo padrão: `text`
- O atributo `name` (obrigatório para envio)
- O atributo `placeholder`

#### Tipos de Input

##### Texto (`type="text"`)

- Campo de texto de linha única
- Atributos: `name`, `placeholder`, `value`

##### Email (`type="email"`)

- Validação de formato de email
- Validação no cliente (navegador)

##### Senha (`type="password"`)

- Ocultação de caracteres digitados
- Uso para campos de senha

##### Números (`type="number"`)

- Aceita apenas números
- Atributos `min` e `max`
- Atributo `step`
- Exemplos práticos

##### Campos Ocultos (`type="hidden"`)

- Campos não visíveis ao usuário
- Enviados com o formulário
- Uso para tokens CSRF, identificação

##### Valor Padrão

- O atributo `value`
- Interação com `placeholder`

---

### Capítulo 16 - Outros Campos de Formulário

#### Uploads de Arquivos (`type="file"`)

- Enviar arquivos ao servidor
- Múltiplos arquivos (`multiple`)
- O atributo `accept`
- Tipos MIME
- Extensões de arquivo

#### Botões

- `type="button"` - Botão genérico
- `type="reset"` - Limpar formulário
- Uso com JavaScript

#### Botões de Rádio (`type="radio"`)

- Escolher uma opção de um grupo
- Mesmo `name`, diferentes `value`
- Atributo `checked`
- Apenas um selecionado por grupo

#### Caixas de Seleção (`type="checkbox"`)

- Escolher zero, uma ou múltiplas opções
- Mesmo `name`, diferentes `value`
- Atributo `checked`
- Múltiplos valores enviados

#### Data e Hora

- `type="date"` - Data
- `type="time"` - Hora
- `type="month"` - Mês e ano
- `type="week"` - Semana e ano
- `type="datetime-local"` - Data e hora
- Limites e steps

#### Seletor de Cores (`type="color"`)

- Escolher cor
- Valor padrão com `value`
- Formato hexadecimal

#### Faixa (`type="range"`)

- Slider para valores
- Atributos `min`, `max`, `value`, `step`

#### Telefone (`type="tel"`)

- Número de telefone
- Teclado numérico em dispositivos móveis
- Validação com `pattern`

#### URL (`type="url"`)

- Campo para URLs
- Validação com `pattern`

#### A Tag `<textarea>`

- Texto multilinha
- Atributos `rows` e `cols`
- Atributo `name`
- Diferença de `<input type="text">`

#### A Tag `<select>`

- Menu suspenso
- Tag `<option>`
- Atributos `name` e `value`
- Opção `disabled`
- Opção vazia
- Tag `<optgroup>` para agrupar opções
- Atributo `label` em `<optgroup>`

---

### Capítulo 17 - Envio e Validação de Formulários

#### Envio de Formulário

- `type="submit"` - Botão de envio
- Atributo `value` (texto do botão)
- Comportamento padrão

#### Validação de Formulário

- Validação no cliente (navegador)
- O atributo `required`
- Campos obrigatórios
- Validação automática de `type="email"`
- Validação de `min` e `max` em números
- O atributo `pattern`
- Expressões regulares para validação
- Mensagens de erro do navegador

---

## PARTE 6: Tabelas e Multimídia

### Capítulo 18 - Tabelas

#### Introdução

- História: tabelas para layout (deprecated)
- Uso atual: apenas para dados tabulares
- CSS para layouts

#### A Tag `<table>`

- Estrutura básica
- Raciocínio em linhas (não colunas)

#### Linhas (`<tr>`)

- Adicionar linhas à tabela
- Múltiplas linhas

#### Cabeçalhos de Coluna (`<th>`)

- Nome das colunas
- Normalmente em negrito
- Primeira linha como cabeçalho

#### Conteúdo da Tabela (`<td>`)

- Dados da tabela
- Dentro de `<tr>`

#### Ampliar Colunas e Linhas

- Atributo `colspan` - Expandir colunas
- Atributo `rowspan` - Expandir linhas
- Exemplos práticos

#### Títulos de Linha

- `<th>` como primeiro elemento em `<tr>`
- Cabeçalhos de linha

#### Organização Avançada

- Tag `<thead>` - Cabeçalho da tabela
- Tag `<tbody>` - Corpo da tabela
- Tag `<tfoot>` - Rodapé da tabela
- Estrutura completa

#### Legenda da Tabela (`<caption>`)

- Descrição da tabela
- Posicionamento (logo após `<table>`)
- Importância para acessibilidade

---

### Capítulo 19 - Multimídia e iframes

#### Tags Multimídia: Áudio e Vídeo

##### A Tag `<audio>`

- Incorporar áudio na página
- O atributo `src`
- O atributo `controls`
- O atributo `type` (MIME)
- O atributo `autoplay`
- O atributo `loop`
- O atributo `muted`
- Eventos JavaScript (play, pause, playing, ended)
- Limitações em dispositivos móveis

##### A Tag `<video>`

- Incorporar vídeo na página
- O atributo `src`
- O atributo `controls`
- O atributo `type` (MIME)
- O atributo `autoplay`
- O atributo `muted` (necessário para autoplay)
- O atributo `loop`
- O atributo `poster` (imagem de capa)
- Atributos `width` e `height`
- Eventos JavaScript (play, pause, playing, ended)

---

#### IFrames

##### Introdução

- Incorporar conteúdo de outras origens
- Contexto de navegação aninhado
- Isolamento (JavaScript e CSS não "vazam")
- Exemplos: Codepen, Glitch

##### Uso Básico

- Tag `<iframe>`
- Atributo `src` (URL relativo ou absoluto)
- Atributos `width` e `height`
- Tamanho padrão (300x150px)

##### O Atributo `srcdoc`

- HTML embutido
- Alternativa ao `src`
- Suporte de navegadores

##### O Atributo `sandbox`

- Limitar operações permitidas
- Valores: `""` (nada permitido) ou opções específicas
- Opções disponíveis:
  - `allow-forms`
  - `allow-modals`
  - `allow-orientation-lock`
  - `allow-popups`
  - `allow-same-origin`
  - `allow-scripts`
  - `allow-top-navigation`

##### O Atributo `allow`

- Futuro do compartilhamento de recursos
- Suporte experimental (Chromium)
- Recursos específicos (câmera, microfone, geolocalização, etc.)

##### O Atributo `referrerpolicy`

- Controlar informações de referrer
- Valores disponíveis:
  - `no-referrer-when-downgrade` (padrão)
  - `no-referrer`
  - `origin`
  - `origin-when-cross-origin`
  - `same-origin`
  - `strict-origin`
  - `strict-origin-when-cross-origin`
  - `unsafe-url`

---

## PARTE 7: Tópicos Avançados

### Capítulo 20 - Acessibilidade

- O que é acessibilidade web
- Por que é importante
- Tags semânticas e acessibilidade
- Atributo `alt` em imagens
- Estrutura de títulos (`<h1>` a `<h6>`)
- Labels em formulários
- Contraste de cores
- Navegação por teclado
- Leitores de tela
- ARIA (conceitos básicos)
- Boas práticas gerais

---

## Conclusão

- Recapitulação dos principais conceitos
- Próximos passos
- Recursos adicionais
- Prática contínua

---

## Apêndices

### Apêndice A - Referência Rápida de Tags

- Lista completa de tags mencionadas
- Descrição breve de cada uma

### Apêndice B - Referência de Atributos Comuns

- Atributos globais
- Atributos específicos por tag

### Apêndice C - Boas Práticas

- Estruturação semântica
- Performance
- SEO
- Acessibilidade
- Manutenibilidade

---

## Notas sobre a Estrutura

### Ordem dos Capítulos

A ordem proposta segue uma progressão lógica:

1. **Fundamentos** - Conceitos básicos necessários para entender tudo que vem depois
2. **Estrutura do Documento** - Como organizar uma página HTML
3. **Conteúdo** - Como adicionar e formatar conteúdo
4. **Estruturação Avançada** - Tags semânticas e organização
5. **Formulários** - Interatividade básica
6. **Tabelas e Multimídia** - Conteúdo mais complexo
7. **Tópicos Avançados** - Acessibilidade e boas práticas

### Pontos Fortes desta Estrutura

- ✅ Progressão do simples ao complexo
- ✅ Cada capítulo constrói sobre os anteriores
- ✅ Conceitos fundamentais primeiro
- ✅ Tópicos práticos depois
- ✅ Tópicos avançados no final

### Sugestões de Melhorias Futuras

- Adicionar exercícios práticos ao final de cada capítulo
- Criar projetos práticos que combinem múltiplos conceitos
- Incluir seção sobre HTML5 APIs básicas (se relevante)
- Adicionar troubleshooting comum
