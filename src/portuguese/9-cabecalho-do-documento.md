# O Cebçalho do Documento

A tag head contém tags exclusivas que definem as propriedades do documento.
É sempre escrito antes da tag body, logo após a tag html de abertura:

```html
<!DOCTYPE html>
<html>
   <head>
     ...
   </head>
   ...
</html>
```

Nunca usamos atributos nesta tag. E não escrevemos conteúdo nele.
É apenas um contêiner para outras tags. Dentro dele, podemos ter uma grande variedade de tags, dependendo do que você precisa fazer:

- title
- script
- noscript
- link
- style
- base
- meta

## A tag title

A tag title determina o título da página. O navegador o exibe e é essencial, pois é um dos fatores críticos para Search Engine Optimization (SEO).

## A tag script

Usamos a tag script para adicionar JavaScript à página.
Você pode incluí-lo em linha, usando uma tag de abertura, o código JavaScript e a tag de fechamento:

```html
<script>
  algum JS...
</script>
```

Ou você pode carregar um arquivo JavaScript externo usando o atributo src:

```html
<script src="file.js"></script>
```

O atributo padrão para type é text/javascript, portanto é totalmente opcional.

Há algo essencial a saber sobre essa tag. Às vezes, essa tag é usada na parte inferior da página, logo antes da tag de fechamento </body>. Por que? Por motivos de desempenho. Os scripts de carregamento, por padrão, bloqueiam a renderização da página até que o script seja analisado e carregado.
Ao colocá-lo na parte inferior da página, o script é carregado e executado após toda a página já ter sido analisada e carregada, proporcionando uma melhor experiência do usuário. Isso agora é uma prática ruim. Deixe o script viver na tag head.
No JavaScript moderno, temos uma alternativa com melhor desempenho do que manter o script no final da página: o atributo defer. Aqui temos um exemplo que carrega um arquivo.js relativo à URL atual:

```html
<script defer src="file.js"></script>
```

O atributo defer aciona o caminho mais rápido para uma página de carregamento rápido e JavaScript de carregamento rápido.

> Nota: o atributo assíncrono é semelhante, mas uma opção pior do que defer. Eu o descrevo com mais detalhes no Ebook de Javascript.