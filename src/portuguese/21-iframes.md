# IFrames

A tag `iframe` nos permite incorporar conteúdo proveniente de outras origens (outros sites) em nossa página web.
Tecnicamente, um iframe cria um novo contexto de navegação aninhado. Isso significa que nada no iframe interfere na página pai e vice-versa. JavaScript e CSS não "vazam" de/para iframes.
Muitos sites usam iframes para realizar várias coisas. Você pode estar familiarizado com Codepen, Glitch ou outros sites que permitem codificar em uma parte da página e ver o resultado em uma caixa. Isso é um iframe.
Você cria um desta maneira:

```html
<iframe src="pagina.html"></iframe>
```

Você também pode carregar um URL absoluto:

```html
<iframe src="https://site.com/pagina.html"></iframe>
```

Você pode definir parâmetros de largura e altura (ou defini-los usando CSS). Caso contrário, o iframe usará o padrão, uma caixa de 300x150 pixels:

```html
<iframe src="pagina.html" width="800" height="400"></iframe>
```

## Srcdoc

O atributo `srcdoc` permite especificar algum HTML embutido para mostrar. É uma alternativa ao `src`, mas recente e não suportada no Edge 18 e inferior e no IE:

```html
<iframe srcdoc="<p>Meu cachorro é um bom cachorro</p>"></iframe>
```

## Sandbox

O atributo `sandbox` nos permite limitar as operações permitidas nos iframes.
Se omitirmos, tudo é permitido:

```html
<iframe src="page.html"></iframe>
```

Se definirmos como "", nada será permitido:

```html
<iframe src="page.html" sandbox=""></iframe>
```

Podemos selecionar o que permitir adicionando opções no atributo `sandbox`. Você pode permitir vários adicionando um espaço entre eles. Aqui está uma lista incompleta das opções que você pode usar:

- `allow-forms` - permite o envio de formulários
- `allow-modals` - permite abrir janelas modais, incluindo chamar `alert()` em javascript
- `allow-orientation-lock` - permite bloquear a orientação da tela
- `allow-popups` - permite pop-ups, usando links `window.open()` e `target="_blank"`
- `allow-same-origin` - trata o recurso carregado como a mesma origem
- `allow-scripts` - permite que o iframe carregado execute scripts (mas não crie pop-ups)
- `allow-top-navigation` - dá acesso ao iframe ao contexto de navegação de nível superior
