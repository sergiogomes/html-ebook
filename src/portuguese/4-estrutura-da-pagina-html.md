# Estrutura da página HTML

Vamos fazer um exemplo de uma página HTML adequada. As coisas começam com a Declaração de Tipo de Documento, uma forma de dizer ao navegador que esta é uma página HTML e qual versão estamos usando.
O HTML moderno usa este tipo de documento:

```html
<!DOCTYPE html>
```

Então temos o elemento html, que possui uma tag de abertura e fechamento:

```html
<!DOCTYPE html>
<html>
   ...
</html>
```

A maioria das tags vem em pares com uma tag de abertura e uma tag de fechamento. Escrevemos a tag de fechamento da mesma forma que a tag de abertura, mas com uma / (barra)

```html
<sometag>algum conteúdo</sometag>
```

Existem algumas tags de fechamento automático, o que significa que elas não precisam de uma tag de fechamento separada, pois não contêm nada. Imagem de exemplo:

```html
<img />
```

Usamos o html como tag inicial no início do documento, logo após a declaração do tipo de documento. A tag de finalização html é a última coisa presente em um documento HTML. Dentro do elemento html, temos dois elementos: head e body:

```html
<!DOCTYPE html>
<html>
   <cabeça>
     ...
   </head>
   <corpo>
     ...
   </body>
</html>
```

Dentro do head, teremos as tags essenciais para a criação de uma página web, como o título, os metadados, CSS e JavaScript interno ou externo. Principalmente coisas que não aparecem diretamente na página, mas apenas ajudam o navegador (ou bots como o bot de pesquisa do Google) a exibi-la corretamente.
Dentro do corpo, teremos o conteúdo da página.
