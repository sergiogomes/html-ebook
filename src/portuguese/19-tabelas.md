# Tabelas

Nos primórdios da web, as tabelas eram uma parte essencial da construção de layouts.
Mais tarde, o CSS substituiu as tabelas por seus recursos de layout, e hoje temos ferramentas poderosas como CSS Flexbox e CSS Grid para construir layouts. Usamos tabelas apenas para, adivinhe, criar tabelas!

## A tag table

Você define uma tabela usando a tag `table`:

```html
<table>
</table>
```

Dentro da tabela, definiremos os dados. Raciocinamos em termos de linhas, o que significa que adicionamos linhas a uma tabela (não colunas). Definiremos colunas dentro de uma linha.

## Linhas

Podemos adicionar uma linha usando a tag `tr`, e essa é a única coisa que podemos adicionar a um elemento de tabela:

```html
<table>
  <tr></tr>
  <tr></tr>
  <tr></tr>
</table>
```

Esta é uma tabela com três linhas.
A primeira linha pode assumir a função de cabeçalho.

## Cabeçalhos de coluna

O cabeçalho da tabela contém o nome de uma coluna, normalmente em negrito.
Pense em um documento Excel/Planilhas Google. O cabeçalho A-B-C-D... superior.
Definimos o cabeçalho usando a tag `th`:

```html
<table>
  <tr>
    <th>Coluna 1</th>
    <th>Coluna 2</th>
    <th>Coluna 3</th>
  </tr>
  <tr></tr>
  <tr></tr>
</table>
```

## O conteúdo da tabela

Definimos o conteúdo da tabela usando tags `td` dentro dos elementos `tr`:

```html
<table>
  <tr>
    <th>Coluna 1</th>
    <th>Coluna 2</th>
    <th>Coluna 3</th>
  </tr>
  <tr>
    <td>Linha 1 Coluna 1</td>
    <td>Linha 1 Coluna 2</td>
    <td>Linha 1 Coluna 3</td>
  </tr>
  <tr>
    <td>Linha 2 Coluna 1</td>
    <td>Linha 2 Coluna 2</td>
    <td>Linha 2 Coluna 3</td>
  </tr>
</table>
```
