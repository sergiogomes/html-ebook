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

O atributo defer diz ao navegador para não esperar pelo script. o navegador continuará a processar o HTML e a criar o DOM enquanto o script é carregado “em segundo plano” e, em seguida, executado quando o DOM estiver totalmente criado.

> Nota: o atributo async é semelhante, mas uma opção pior do que defer. Eu o descrevo com mais detalhes no Ebook de Javascript.

## A tag noscript

A tag noscript detecta quando os scripts estão desabilitados no navegador.

> Observação: os usuários podem optar por desativar os scripts JavaScript nas configurações do navegador. Ou o navegador pode não suportá-los por padrão.

Ele é usado de forma diferente dependendo se é colocado no cabeçalho do documento ou no corpo do documento. Estamos falando sobre o cabeçalho do documento agora, então vamos primeiro apresentar esse uso.
Nesse caso, a tag noscript só pode conter outras tags:

- tags de link
- tags de style
- tags de meta

Para alterar os recursos servidos pela página, ou a meta informação, se os scripts estiverem desabilitados.
Neste exemplo, defino um elemento com a classe no-script-alert para exibir se os scripts estiverem desabilitados, como era display: none por padrão:

```html
<!DOCTYPE html>
<html>
  <head>
    ...
    <noscript>
      <style>
        .no-script-alert {
          display: block;
        }
      </style>
    </noscript>
    ...
  </head>
  ...
</html>
```

Vamos resolver o outro caso: se colocado no corpo, pode conter conteúdo, como parágrafos e outras tags, e renderizar na interface do usuário.

## A tag de link

Usamos a tag de link para definir relacionamentos entre um documento e
outros recursos, usados principalmente para vincular um arquivo CSS externo a ser carregado. Este elemento não tem tag de fechamento.
Uso:

```html
<!DOCTYPE html>
<html>
   <head>
     ...
     <link href="file.css" rel="stylesheet">
     ...
   </head>
   ...
</html>
```

O atributo media permite o carregamento de diferentes folhas de estilo dependendo das capacidades do dispositivo:

```html
<link href="file.css" media="screen" rel="stylesheet">
<link href="print.css" media="print" rel="stylesheet">
```

Também podemos vincular a outros recursos além de folhas de estilo. Por exemplo, podemos associar um feed RSS usando

```html
<link rel="alternate" type="application/rss+xml" href="/index.xml">
```

Ou podemos associar um favicon usando:

```html
<link rel="apple-touch-icon" sizes="180x180" href="/assets/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/assets/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/assets/favicon-16x16.png">
```

Também podemos usar a tag de link para conteúdo de várias páginas, indicando a página anterior e a seguinte com rel="prev" e rel="next", principalmente para o Google. A partir de 2019, o Google anunciou que não usa mais esta tag: <https://twitter.com/googlewmc/status/1108726443251519489> porque pode encontrar a estrutura de página correta sem ela.

## A tag de style

Podemos usar a tag style para adicionar estilos ao documento em vez de carregar uma folha de estilo externa. Uso:

```html
<style>
   .some-css {}
</style>
```

Assim como a tag link, você pode usar o atributo media para usar aquele CSS apenas na mídia especificada:

```html
<style media="print">
   .some-css {}
</style>
```

## A tag base

Podemos usar a tag base para definir um URL base para todos os URLs relativos contidos na página.

```html
<!DOCTYPE html>
<html>
   <head>
     ...
     <base href="https://www.sergiogomes.com/">
     ...
   </head>
   ...
</html>
```

## A meta tag

Meta tags executam várias tarefas e são importantes, especialmente para SEO. Os elementos meta têm apenas a tag inicial. A mais básica é a meta tag de descrição:

```html
<meta name="description" content="Uma bela página">
```

O Google pode usar isso para gerar a descrição da página em suas páginas de resultados se achar que descreve melhor a página do que o conteúdo na página.
Podemos usar o charset meta para definir a codificação de caracteres da página. UTF-8 na maioria dos casos:

```html
<meta charset="utf-8">
```

A metatag robots instrui os bots do mecanismo de pesquisa se devem ou não indexar uma página:

```html
<meta name="robots" content="noindex">
```

Ou se devem seguir links ou não:

```html
<meta name="robots" content="nofollow">
```

Você pode combiná-los:

```html
<meta name="robots" content="noindex, nofollow">
```

O comportamento padrão é index, follow.
Você pode usar outras propriedades, incluindo nosnippet, noarchive, noimageindex e muito mais.
Você também pode dizer ao Google em vez de segmentar todos os mecanismos de pesquisa:

```html
<meta name="googlebot" content="noindex, nofollow">
```

Outros mecanismos de pesquisa também podem ter sua própria metatag.
Falando nisso, podemos dizer ao Google para desativar alguns recursos. A meta tag notranslate impede a funcionalidade de tradução nos resultados do mecanismo de pesquisa:

```html
<meta name="google" content="notranslate">
```

Podemos usar a meta tag viewport para informar ao navegador para definir a largura da página com base na largura do dispositivo.

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

Veja mais sobre esta tag: <https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag>.

Outra meta tag bastante popular é a http-equiv="refresh". Esta linha diz ao navegador para esperar 3 segundos e redirecionar para a outra página:

```html
<meta http-equiv="refresh" content="3;url=http://www.sergiogomes.com/another-page">
```

Usar 0 em vez de 3 redirecionará o mais rápido possível.

Após a introdução deste documento, podemos começar a mergulhar no corpo do documento: body.
