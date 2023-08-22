# Envio de formulário

O campo com `type="submit"` é um botão que, uma vez pressionado pelo usuário, envia o formulário:

```html
<input type="submit">
```

O atributo `value` define o texto no botão, que, se ausente, mostra o texto "Submit":

```html
<input type="submit" value="Clique em mim">
```

## Validação de formulário

Os navegadores fornecem funcionalidade de validação do lado do cliente para formulários.
Podemos definir os campos como `required`, garantindo que não estejam vazios e aplicar um formato específico para a entrada de cada campo.
Vamos ver as duas opções.

### Defina os campos como required

O atributo `required` nos ajuda na validação. Se o usuário não preencher o campo, a validação do lado do cliente falha e o navegador não envia o formulário:

```html
<input type="text" name="nome-usuario" required>
```

### Aplicar um formato específico

Eu descrevi o campo `type="email"` acima. Ele valida automaticamente o endereço de e-mail de acordo com um formato definido na especificação.
No campo `type="number"`, mencionei o atributo `min` e `max` para limitar os valores inseridos a um intervalo.
Podemos fazer mais.
Podemos impor um formato específico em qualquer campo.
O atributo `pattern` nos permite definir uma expressão regular para validar o valor.
Recomendo a leitura do meu Guia de Expressões Regulares em <https://www.sergiopgomes.com/javascript-regular-expressions/>.
padrão="https://.*"

```html
<input type="text" name="nome-usuario" pattern="[a-zA-Z{8}">
```
