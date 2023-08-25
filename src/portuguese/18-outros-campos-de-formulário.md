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
