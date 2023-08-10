# Links

Os links são definidos usando a tag `a`. Definimos seu destino por meio do atributo `href`.
Exemplo:

```html
<a href="https://www.sergiopgomes.com">Clique aqui</a>
```

Temos o texto do link Entre as tags inicial e final.
O exemplo acima é um URL absoluto, mas os links também funcionam com URLs relativos:

```html
<a href="/sobre">clique aqui</a>
```

Nesse caso, ao clicar no link, o usuário é movido para a URL `/sobre` na origem atual.
Tenha cuidado com o caractere `/`. Se omitido, o navegador adicionará a sequência de texto à URL atual em vez de começar pela origem.
Por exemplo, estou na página <https://www.sergiopgomes.com/axios/> e tenho estes links:

- /sobre uma vez clicado me leva a <https://www.sergiopgomes.com/sobre>
- sobre uma vez clicado me leva a <https://www.sergiopgomes.com/axios/sobre>

As tags de link podem incluir outras coisas dentro delas, não apenas texto. Por exemplo, imagens:

```html
<a href="https://www.sergiopgomes.com/">
  <img src="avatar.jpg">
</a>
```

Ou quaisquer outros elementos, exceto outras tags `a`.
Se você quiser abrir o link em uma nova aba, você pode usar o atributo `target`:

```html
<a href="https://www.sergiopgomes.com/" target="_blank">
  Abrir em uma nova guia
</a>
```
