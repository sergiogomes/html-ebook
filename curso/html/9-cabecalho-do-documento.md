# Cabeçalho do documento (`head`)

## Objetivo da aula

Ao final desta aula, você vai conseguir:

- Entender para que serve o elemento `<head>` e onde ele fica no HTML
- Saber quais tags são comuns dentro do `head` e o que cada uma faz
- Usar `script` com `defer` do jeito recomendado
- Entender o básico de meta tags importantes (SEO, charset, viewport, robots)

---

## 1) O que é o `head` (e onde fica)

A tag `head` contém tags que definem propriedades do documento.

Ela é sempre escrita antes da tag `body`, logo após a tag `html` de abertura:

```html
<!DOCTYPE html>
<html>
  <head>
    ...
  </head>
  ...
</html>
```

No `head`, a regra geral é:

- Você **não escreve conteúdo visível** (texto “da página”) ali
- Ele funciona como um **contêiner** para outras tags (metadados e recursos)

Dentro dele, podemos ter uma grande variedade de tags, dependendo do que você precisa:

- `title`
- `script`
- `noscript`
- `link`
- `style`
- `base`
- `meta`

---

## 2) `title`

A tag `title` determina o título da página.

O navegador exibe esse título (normalmente na aba) e ele é importante porque influencia SEO.

Faixa prática recomendada para SEO:

- `title`: entre **50 e 60 caracteres** (aprox.)

Exemplo:

```html
<title>Minha página</title>
```

---

## 3) `script` (JavaScript no documento)

Usamos a tag `script` para adicionar JavaScript à página.

Você pode incluir JS inline:

```html
<script>
  // algum JS...
</script>
```

Ou carregar um arquivo externo com `src`:

```html
<script src="file.js"></script>
```

O atributo `type` hoje costuma ser desnecessário: o padrão é `text/javascript`.

### Por que você vai ver `<script>` no fim do `body`?

Historicamente, muita gente colocava scripts no final do documento, logo antes do `</body>`, por desempenho:

- Por padrão, o navegador pode **parar a renderização** para baixar e processar scripts.

Hoje, a abordagem mais recomendada (e mais limpa) é manter o script no `head` e usar `defer`:

```html
<script defer src="file.js"></script>
```

Com `defer`, o navegador:

- continua processando o HTML e criando o DOM
- baixa o script “em segundo plano”
- executa o script quando o DOM estiver pronto

> Nota: o atributo `async` é parecido, mas geralmente dá menos previsibilidade do que `defer`.

---

## 4) `noscript`

A tag `noscript` é usada para situações em que scripts estão desabilitados no navegador.

> Observação: usuários podem desativar JavaScript nas configurações, ou o ambiente pode não suportar scripts.

O uso muda dependendo de onde ela aparece. No `head`, ela só pode conter:

- tags `link`
- tags `style`
- tags `meta`

Exemplo (no `head`): mostrar um alerta caso scripts estejam desabilitados (via CSS):

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

Se você colocar `noscript` no `body`, aí sim ele pode conter conteúdo visível (parágrafos, etc.) e renderizar na interface.

---

## 5) `link` (relacionar recursos com o documento)

A tag `link` define relacionamentos entre o documento e outros recursos, principalmente para carregar CSS externo.

Ela não tem tag de fechamento.

Exemplo:

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

O atributo `media` permite carregar estilos dependendo do tipo de mídia:

```html
<link href="file.css" media="screen" rel="stylesheet">
<link href="print.css" media="print" rel="stylesheet">
```

Outros usos comuns:

- RSS:

RSS (*Really Simple Syndication*) é um formato para distribuir atualizações de conteúdo (como posts e notícias) para leitores/aggregators.

```html
<link rel="alternate" type="application/rss+xml" href="/index.xml">
```

- Favicon:

```html
<link rel="apple-touch-icon" sizes="180x180" href="/assets/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/assets/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/assets/favicon-16x16.png">
```

Você também vai ver `rel="prev"` e `rel="next"` em alguns sites, mas o Google anunciou em 2019 que não usa mais isso como sinal: <https://twitter.com/googlewmc/status/1108726443251519489>.

---

## 6) `style` (CSS no próprio documento)

Podemos usar a tag `style` para adicionar CSS direto no documento, sem arquivo externo:

```html
<style>
  .some-css {}
</style>
```

Assim como em `link`, dá pra usar `media`:

```html
<style media="print">
  .some-css {}
</style>
```

---

## 7) `base` (URL base para links relativos)

Podemos usar `base` para definir um URL base para todos os URLs relativos contidos na página:

```html
<!DOCTYPE html>
<html>
  <head>
    ...
    <base href="https://www.sergiopgomes.com/">
    ...
  </head>
  ...
</html>
```

---

## 8) `meta` (metadados, SEO e comportamento)

Meta tags executam várias tarefas e são importantes, especialmente para SEO.  
Elementos `meta` têm apenas tag inicial.

### Descrição (SEO)

```html
<meta name="description" content="Uma bela página">
```

O Google pode usar isso como descrição nos resultados se achar que descreve melhor a página do que o conteúdo visível.

Faixa prática recomendada para SEO:

- `meta description`: entre **140 e 160 caracteres** (aprox.)
- Em telas menores, o corte pode acontecer antes

### Charset (codificação)

```html
<meta charset="utf-8">
```

Na maioria dos casos, **UTF-8** é o que você quer.

> **UTF-8** é o "dicionário" que o navegador usa pra converter bytes em caracteres legíveis. Na prática, garante que caracteres como ç, ã, é, emojis, etc, sejam interpretados corretamente.

### Robots (indexação e links)

```html
<meta name="robots" content="noindex">
```

Ou para links:

```html
<meta name="robots" content="nofollow">
```

Você pode combinar:

```html
<meta name="robots" content="noindex, nofollow">
```

O padrão é `index, follow`.

O que isso significa, na prática:

- **Indexar** (`index` / `noindex`): permite ou impede que a página entre no índice do buscador (ou seja, apareça nos resultados).
- **Seguir links** (`follow` / `nofollow`): permite ou impede que o crawler use os links dessa página para descobrir outras URLs e associar sinais.

Combinações comuns:

- `index, follow`: padrão para páginas públicas.
- `noindex, follow`: a página não aparece, mas os links ainda podem ser usados para descoberta.
- `noindex, nofollow`: a página não aparece e também não “serve de ponte” para rastrear links.

E você pode segmentar o Google:

```html
<meta name="googlebot" content="noindex, nofollow">
```

### Notranslate

```html
<meta name="google" content="notranslate">
```

Isso pede para o Google **não oferecer tradução automática** dessa página nos resultados de busca (útil quando tradução pode atrapalhar termos técnicos ou branding).

### Viewport (mobile)

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

Esse `meta` diz ao navegador como calcular o “tamanho” da página em telas pequenas. Sem ele, é comum o celular renderizar como se fosse uma tela larga (desktop) e diminuir tudo, deixando texto pequeno e a página “zoada”.

Link de referência: <https://developer.mozilla.org/en-US/docs/Web/HTML/Viewport_meta_tag>.

### Refresh (redirecionamento)

```html
<meta http-equiv="refresh" content="3;url=http://www.sergiopgomes.com">
```

Usar `0` no lugar de `3` redireciona o mais rápido possível.

---

## 9) Mini-exercício (3 minutos)

Crie um `index.html` completo e coloque, no `head`:

- Um `<title>`
- `<meta charset="utf-8">`
- `<meta name="viewport" ...>`
- Um `<meta name="description" ...>`
- Um `<link rel="icon" ...>` (pode apontar pra um arquivo que você ainda vai criar)
- Um `<script defer src="app.js"></script>`

Depois:

- Abra no navegador e confira o título da aba.
- Abra o “Exibir código-fonte” e confirme que suas tags estão no `head`.

---

## 10) Fechamento

- O `head` guarda metadados e recursos do documento.
- `title` é importante para o navegador e para SEO.
- Scripts no `head` com `defer` dão um fluxo mais previsível e performático.
- `link`, `style`, `base` e `meta` são ferramentas essenciais do `head`.
- Depois do `head`, a gente entra no `body`, que é o conteúdo visível da página.
