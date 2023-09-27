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

## Ampliar colunas e linhas

Podemos ter uma linha abrangendo duas ou mais colunas usando o atributo `colspan`:

```html
<table>
  <tr>
    <th>Coluna 1</th>
    <th>Coluna 2</th>
    <th>Coluna 3</th>
  </tr>
  <tr>
    <td colspan="2">Linha 1 Colunas 1-2</td>
    <td>Linha 1 Coluna 3</td>
  </tr>
  <tr>
    <td colspan="3">Linha 2 Colunas 1-3</td>
  </tr>
</table>
```

Ou pode abranger duas ou mais linhas usando o atributo `rowspan`:

```html
<table>
  <tr>
    <th>Coluna 1</th>
    <th>Coluna 2</th>
    <th>Coluna 3</th>
  </tr>
  <tr>
    <td colspan="2" rowspan="2">Linhas 1-2 Colunas 1-2</td>
    <td>Linha 1 Coluna 3</td>
  </tr>
  <tr>
    <td>Linha 2 Coluna 3</td>
  </tr>
</table>
```

## Títulos de linha

Podemos adicionar uma tag `th` como o primeiro elemento dentro de um `tr` que não é o primeiro `tr` da tabela a ter cabeçalhos de linha:

```html
<table>
  <tr>
    <th></th>
    <th>Coluna 2</th>
    <th>Coluna 3</th>
  </tr>
  <tr>
    <th>Linha 1</th>
    <td>Coluna 2</td>
    <td>Coluna 3</td>
  </tr>
  <tr>
    <th>Linha 2</th>
    <td>Coluna 2</td>
    <td>Coluna 3</td>
  </tr>
</table>
```

## Mais tags para organizar a mesa

Você pode adicionar mais três tags a uma tabela para deixá-la mais organizada. Isso é melhor ao usar mesas grandes. E para definir corretamente um cabeçalho e um rodapé também.
Essas tags são

- `thead`
- `tcorpo`
- `tpé`

Eles envolvem as tags `tr` para definir claramente as diferentes seções da tabela. Aqui está um exemplo:

```html
<table>
  <thead>
    <tr>
      <th></th>
      <th>Coluna 2</th>
      <th>Coluna 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Linha 1</th>
      <td>Coluna 2</td>
      <td>Coluna 3</td>
    </tr>
    <tr>
      <th>Linha 2</th>
      <td>Coluna 2</td>
      <td>Coluna 3</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td></td>
      <td>Rodapé da coluna 1</td>
      <td>Rodapé da coluna 2</td>
    </tr>
  </tfoot>
</table>
```

## Legenda da tabela

Uma tabela deve ter uma tag `caption` que descreva seu conteúdo. Devemos colocar esta tag imediatamente após a tag de abertura `table`:

```html
<table>
  <caption>Idade dos cães</caption>
  <tr>
    <th>Cachorro</th>
    <th>Idade</th>
  </tr>
  <tr>
    <td>Rogério</td>
    <td>7</td>
  </tr>
</table>
```
