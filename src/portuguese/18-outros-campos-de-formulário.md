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

## Data e hora

Temos alguns tipos de entrada para aceitar valores de data.
O campo de entrada `type="date"` permite ao usuário inserir uma data e mostra um seletor de data, se necessário:

```html
<input type="date" name="aniversario">
```

O campo de entrada `type="time"` permite ao usuário inserir um horário e mostra um seletor de horário, se necessário:

```html
<input type="time" name="horario-de-entrega">
```

O campo de entrada `type="month"` permite ao usuário inserir um mês e um ano:

```html
<input type="month" name="escolha-mes-lancamento">
```

O campo de entrada `type="week"` permite ao usuário inserir uma semana e um ano:

```html
<input type="week" name="escolher-semana">
```

Todos esses campos permitem limitar o intervalo e o passo entre cada valor. Eu recomendo verificar o site do MDN para obter detalhes específicos de cada um.

O campo `type="datetime-local"` permite escolher uma data e uma hora.

```html
<input type="datetime-local" name="data-e-hora">
```

## Seletor de cores

Você pode permitir que os usuários escolham uma cor usando o elemento `type="color"`:

```html
<input type="color" name="cor-do-carro">
```

Você define um valor padrão usando o atributo `value`:

```html
<input type="color" name="cor-do-carro" value="#000000">
```

O navegador se encarregará de mostrar um seletor de cores ao usuário.

## Faixa

Este elemento de entrada mostra um `slider`. As pessoas podem usá-lo para passar de um valor inicial para um valor final:

```html
<input type="range" nome="idade" min="0" max="100" valor="30">
```

Você pode fornecer uma `step` opcional:

```html
<input type="range" nome="idade" min="0" max="100" valor="30" step=
"10">
```

## Telefone

Podemos usar o campo de entrada `type="tel"` para inserir um número de telefone:

```html
<input type="tel" name="numero-telefone">
```

A principal diferença tipo de entrada do `tel` para o do `texto` é o comportamento no celular, onde o dispositivo pode optar por mostrar um teclado numérico.

Especifique um atributo `pattern` para validação adicional:

```html
<input type="tel" pattern="[0-9]{3}-[0-9]{8}" name="numero-telefone">
```

## URL

Podemos usar o campo `type="url"` para inserir uma URL.

```html
<input type="url" name="website">
```

Podemos validá-lo usando o atributo `pattern`:

```html
<input type="url" name="website" pattern="https://.*">
```

## A tag textarea

O elemento `textarea` permite aos usuários inserir texto multilinha. Comparado com `input`, requer uma tag final:

```html
<textarea></textarea>
```

Você pode definir as dimensões usando CSS, mas também usando os atributos `rows` e `cols`:

```html
<textarea rows="20" cols="10"></textarea>
```

Tal como acontece com as outras tags de formulário, o atributo `name` determina o nome nos dados enviados ao servidor:

```html
<textarea name="artigo"></textarea>
```

## A tag select

Podemos usar esta tag para criar um menu suspenso.
O usuário pode escolher uma das opções disponíveis.
Criamos cada opção usando a tag `option`. Adicionamos um `nome` ao select e um `value` a cada opção:

```html
<select name="cor">
  <option value="vermelho">Vermelho</option>
  <option value="amarelo">Amarelo</option>
</select>
```

Você pode definir uma opção `disabled`:

```html
<select name="cor">
  <option value="vermelho" disabled>Vermelho</option>
  <option value="amarelo">Amarelo</option>
</select>
```

Você pode ter uma opção vazia:

```html
<select name="cor">
  <option value="">Nenhum</option>
  <option value="vermelho">Vermelho</option>
  <option value="amarelo">Amarelo</option>
</select>
```

Podemos agrupar opções usando a tag `optgroup`. Cada grupo de opções possui um atributo `label`:

```html
<select name="cor">
  <optgroup label="Primario">
    <option value="vermelho">Vermelho</option>
    <option value="amarelo">Amarelo</option>
    <option value="azul">Azul</option>
  </optgroup>
  <optgroup label="Outros">
    <option value="verde">Verde</option>
    <option value="rosa">Rosa</option>
  </optgroup>
</select>
```
