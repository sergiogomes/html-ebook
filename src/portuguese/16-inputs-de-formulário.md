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
<input type="text" name="nome-usuario">
```

Usamos o atributo `placeholder` para mostrar algum texto em cinza claro quando o campo está vazio. Útil para adicionar uma dica ao usuário sobre o que digitar:

```html
<input type="text" name="nome-usuario" placeholder="Seu nome de usuário">
```

## Email

Usar `type="email"` validará do lado do cliente (no navegador) um e-mail quanto à correção (correção semântica, não garantindo que o endereço de e-mail exista) antes de enviar.

```html
<input type="email" name="email" placeholder="Seu e-mail">
```

## Password

Usar `type="password"` fará com que cada tecla digitada apareça como um asterisco (`*`) ou ponto, útil para campos que hospedam uma senha.

```html
<input type="password" name="senha" placeholder="Sua senha">
```

## Números

Podemos ter um elemento `input` aceitando apenas números:

```html
<input type="number" name="age" placeholder="Sua idade">
```

Podemos especificar um valor `mínimo` e `máximo` aceito:

```html
<input type="number" name="idade" placeholder="Sua idade" min="18" max="110">
```

O atributo `step` ajuda a identificar as etapas entre valores diferentes. No exemplo abaixo, aceitamos um valor entre 10 e 50 em etapas de 5:

```html
<input type="number" name="idade" min="10" max="50" step="5">
```

## Campos ocultos

Podemos ocultar campos do usuário. O `form` os enviará junto com os outros campos visíveis:

```html
<input type="hidden" name="campo-oculto" value="valor">
```

Normalmente usamos para armazenar valores como um token CSRF para segurança e identificação do usuário ou até mesmo para detectar robôs enviando spam usando técnicas especiais.
Também podemos usá-lo para identificar um `form` e sua ação.

## Definindo um valor padrão

Todos esses campos aceitam um valor predefinido. Caso o usuário não altere, este será o `value` enviado ao servidor:

```html
<input type="number" name="idade" value="18">
```

Se você definir um `placeholder`, ele só aparecerá se o usuário limpar o campo de entrada `value`:

```html
<input type="number" name="idade" placeholder="Sua idade" value="18">
```
