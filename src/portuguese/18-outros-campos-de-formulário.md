# Outros Campos de Formulário

## Uploads de arquivos

Você pode carregar arquivos do seu computador local e enviá-los ao servidor usando um elemento de entrada `type="file"`:

```html
<input type="file" name="documentos-secretos">
```

Você pode anexar vários arquivos:

```html
<input type="file" nome="documentos-secretos" multiple>
```

Você pode especificar um ou mais tipos de arquivos permitidos usando o atributo `accept`. Este aceita imagens:

```html
<input type="file" name="documentos-secretos" accept="image/*">
```

Você pode usar um tipo `MIME` específico, como `application/json`, ou definir uma extensão de arquivo como .pdf. Ou definir várias extensões de arquivo como esta:

```html
<input type="file" nome="documentos-secretos" aceitar=".jpg, .jpeg, .png">
```

## Botões

Podemos usar os campos de entrada `type="button"` para adicionar botões ao formulário que não sejam botões de envio:

```html
<input type="button" value="Clique em mim">
```

Eles são usados para fazer algo programaticamente usando JavaScript.

Existe um campo especial renderizado como botão, cuja ação especial é limpar todo o formulário e trazer de volta o estado dos campos ao inicial:

```html
<input type="reset">
```

## Botões de rádio

Podemos usar botões de rádio para criar um conjunto de opções, das quais selecionamos uma opção e todas as outras são desabilitadas.
O nome vem de rádios de carros antigos que possuíam esse tipo de interface.
Você define um conjunto de entradas `type="radio"`, todas com o mesmo atributo `name` e diferentes atributos `value`:

```html
<input type="radio" name="color" value="yellow">
<input type="radio" name="color" value="red">
<input type="radio" name="color" value="blue">
```

Depois que o formulário for enviado, a propriedade de dados `color` terá apenas um valor. Sempre há um elemento verificado. O primeiro item é aquele marcado por padrão. Você pode definir o valor pré-selecionado usando o atributo `checked`. Você pode usá-lo apenas uma vez por grupo de entrada de rádio.

## Caixas de seleção

Assim como os botões de rádio, as caixas de seleção podem criar um conjunto de opções, mas podemos escolher vários valores ou nenhum.
Podemos definir um conjunto de entradas `type="checkbox"`, todas com o mesmo atributo `name` e diferentes atributos `value`:
Todas as caixas de seleção estão desmarcadas por padrão. Use o atributo `checked` para marca-lás no carregamento da página.

```html
<input type="checkbox" name="color" value="yellow">
<input type="checkbox" name="color" value="red">
<input type="checkbox" name="color" value="blue" checked>
```

Como este campo de entrada permite vários valores, o formulário envia os valores para o servidor como uma lista no momento do envio do formulário.
