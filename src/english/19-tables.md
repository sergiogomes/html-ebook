# Tables

In the early days of the web, tables were an essential part of building layouts.
Later, CSS replaced tables with its layout capabilities, and today we have powerful tools like CSS Flexbox and CSS Grid to build layouts. We use tables just for, guess what, creating tables!

## The table tag

You define a table using the `table` tag:

```html
<table>
</table>
```

Inside the table, we'll define the data. We reason in terms of rows, which means we add rows into a table (not columns). We'll define columns inside a row.

## Rows

We can add a row using the `tr` tag, and that's the only thing we can add to a table element:

```html
<table>
  <tr></tr>
  <tr></tr>
  <tr></tr>
</table>
```

This is a table with three rows.
The first row can take the role of the header.

## Column headers

The table header contains the name of a column, typically in bold font.
Think about an Excel / Google Sheets document. The top A-B-C-D... header.
We define the header using the `th` tag:

```html
<table>
  <tr> 
    <th>Column 1</th>
    <th>Column 2</th>
    <th>Column 3</th>
  </tr>
  <tr></tr> 
  <tr></tr>
</table>
```
