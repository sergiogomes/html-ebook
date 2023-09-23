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
