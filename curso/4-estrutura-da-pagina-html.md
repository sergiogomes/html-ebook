# Estrutura da Página HTML

Nesta aula, vamos montar uma página HTML "do jeito certo". Tudo começa com o navegador sabendo que aquele arquivo é HTML.

Vamos fazer um exemplo de uma página HTML adequada. Tudo começa com a Declaração de Tipo de Documento, uma forma de dizer ao navegador que esta é uma página HTML e qual versão estamos usando.

O HTML moderno usa este tipo de documento:

```html
<!DOCTYPE html>
```

## O que acontece se não colocarmos `<!DOCTYPE html>` no topo do arquivo?

Sem o `<!DOCTYPE html>`, o navegador pode deixar de usar o modo "padrões" e passar para um modo mais "antigo" (geralmente chamado de *quirks mode*). Isso pode mudar detalhes de como a página é renderizada, principalmente regras e estilos padrão do navegador (por exemplo, larguras, margens e alguns comportamentos de layout).

Na prática, quando você esquece o `<!DOCTYPE html>`, a página ainda pode aparecer "ok", mas o risco de inconsistências aumenta: CSS e HTML podem se comportar de um jeito diferente do esperado, especialmente quando você compara com outros navegadores ou com tutoriais/códigos mais antigos.

Por isso, em qualquer página HTML moderna, o melhor hábito é colocar o `<!DOCTYPE html>` no topo do arquivo, antes da tag `<html>`.

Então temos o elemento `<html>`, que possui uma tag de abertura e fechamento:

```html
<!DOCTYPE html>
<html>
   ...
</html>
```

A maioria das tags vem em pares com uma tag de abertura e uma tag de fechamento. Escrevemos a tag de fechamento da mesma forma que a tag de abertura, mas com uma `/` (barra):

```html
<sometag>algum conteúdo</sometag>
```

Existem algumas tags de fechamento automático, o que significa que elas não precisam de uma tag de fechamento separada, pois não contêm nada. Imagem de exemplo:

```html
<img />
```

Usamos a tag `html` como tag inicial no início do documento, logo após a declaração do tipo de documento. A tag de finalização `html` é a última coisa presente em um documento HTML.

Dentro do elemento `html`, temos dois elementos: `head` e `body`:

```html
<!DOCTYPE html>
<html>
   <head>
     ...
   </head>
   <body>
     ...
   </body>
</html>
```

Dentro do `head`, teremos as tags essenciais para a criação de uma página web, como o título, os metadados, CSS e JavaScript interno ou externo. Principalmente coisas que não aparecem diretamente na página, mas apenas ajudam o navegador (ou bots como o bot de pesquisa do Google) a exibi-la corretamente.

Dentro do `body`, teremos o conteúdo da página.
