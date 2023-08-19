# Inputs de formulário

## A tag input

O campo `input` é um dos elementos de formulário mais usados. Também é um elemento versátil e pode mudar seu comportamento com base no atributo `type`.
O comportamento padrão é ser um controle de entrada de texto de linha única:

```html
<input>
```

Equivalente a usar:

```html
<input type="text">
```

Assim como todos os outros campos a seguir, precisamos dar um `name` ao campo para que seu conteúdo seja enviado ao servidor quando o `form` for enviado:

```html
<input type="text" name="username">
```

Usamos o atributo `placeholder` para mostrar algum texto em cinza claro quando o campo está vazio. Útil para adicionar uma dica ao usuário sobre o que digitar:

```html
<input type="text" name="nome de usuário" placeholder="Seu nome de usuário">
```
