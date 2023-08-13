# Formulários

Os formulários são como interagimos com uma página ou um aplicativo criado com tecnologias da Web.
Temos um conjunto de controles e, quando você envia o formulário, seja com um clique no botão "enviar" ou programaticamente, o navegador envia os dados para o servidor.
Por padrão, esse envio de dados faz com que a página seja recarregada após o envio dos dados. Mas usando JavaScript, podemos alterar esse comportamento usando `event.preventDefault()`.
Criamos um formulário usando a tag `form`:

```html
<form>
   ...
</form>
```

Por padrão, o `form` é enviado usando o método HTTP `GET`. Que tem suas desvantagens e, geralmente, queremos usar `POST`.
Podemos definir o formulário para usar `POST` quando enviado usando o atributo `method`:

```html
<form method="POST">
   ...
</form>
```

O formulário é enviado, usando `GET` ou `POST`, para a mesma URL onde reside.
Portanto, se o formulário estiver na página <https://www.sergiopgomes.com/contacts>, pressionar o botão "enviar" solicitará a URL exata, o que pode resultar em nada.
Precisamos de algo do lado do servidor para lidar com a solicitação e, normalmente, "escutamos" esses eventos de envio de formulário em uma URL dedicada.
Você pode especificar a URL por meio do parâmetro `action`:

```html
<form action="/novo-contato" method="POST">
   ...
</form>
```

Isso fará com que o navegador envie os dados do formulário usando `POST` para a URL /novo-contato na origem exata.
Se a `origem` (protocolo + domínio + porta) for <https://www.sergiopgomes.com> (porta 80 é o padrão), os dados do formulário serão enviados para <https://www.sergiopgomes.com/novo-contato>.
Eu falei sobre dados. Quais dados?
Os usuários fornecem dados por meio do conjunto de controles disponíveis na plataform Web:

- caixas de entrada (texto de linha única)
- áreas de texto (texto multilinha)
- caixas de seleção (escolha uma opção no menu suspenso)
- botões de rádio (escolha uma opção de uma lista sempre visível)
- caixas de seleção (escolha zero, uma ou mais opções)
- upload de arquivos
- e mais!

Vamos apresentar cada um deles na visão geral dos campos de formulário a seguir.
