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
