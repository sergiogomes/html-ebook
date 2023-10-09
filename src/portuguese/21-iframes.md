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

## Allow

Atualmente suportado apenas por navegadores baseados em Chromium e ainda experimental, este é o futuro do compartilhamento de recursos entre a janela pai e o iframe.
É semelhante ao atributo `sandbox`, mas podemos permitir recursos específicos, incluindo:

- `accelerometer` - dá acesso à interface do Sensors API Accelerometer
- `ambient-light-sensor` - dá acesso à interface Sensors API AmbientLightSensor
- `autoplay` - permite a reprodução automática de arquivos de vídeo e áudio
- `camera` - permite acesso à câmera a partir da API getUserMedia
- `display-capture` - permite acesso ao conteúdo da tela usando a API getDisplayMedia
- `fullscreen` - permite acesso ao modo de tela cheia
- `geolocation` - permite acesso à API de geolocalização
- `gyroscope` - dá acesso à interface Sensors API Gyroscope
- `magnetometer` - dá acesso à interface Sensors API Magnetometer
- `microfone` - dá acesso ao microfone do dispositivo usando a API getUserMedia
- `midi` - permite acesso à API Web MIDI
- `payment` - dá acesso à API de solicitação de pagamento
- `speaker` - permite acesso à reprodução de áudio através dos alto-falantes do dispositivo
- `usb` - dá acesso à API WebUSB.
- `vibrate` - dá acesso à API Vibration
- `vr` - dá acesso à API WebVR

## Referrer

Ao carregar um iframe, o navegador envia informações essenciais sobre quem o carrega no cabeçalho `Referer` (observe o único `r`, um erro de digitação com o qual devemos conviver).

> O erro ortográfico do "referrer" originou-se na proposta original do cientista da computação Phillip Hallam-Baker de incorporar o campo na especificação HTTP. O erro ortográfico foi gravado na pedra no momento de sua incorporação no documento de padrões de Solicitação de Comentários RFC 1945

O atributo `referrerpolicy` nos permite definir o referenciador para enviar ao iframe ao carregá-lo. O referenciador é um cabeçalho HTTP que permite à página saber quem a está carregando. Estes são os valores permitidos:

- `no-referrer-when-downgrade` - é o padrão e não envia o referenciador quando a página atual carrega via HTTPS e o iframe carrega no protocolo HTTP
- `no-referrer` - não envia o cabeçalho do referenciador
- `origin` - o referenciador enviado contém apenas a origem (porta, protocolo, domínio), não a origem + caminho, que é o padrão
- `origin-when-cross-origin` - ao carregar da mesma origem (porta, protocolo, domínio) no iframe, o referenciador tem sua forma completa (origem + caminho). Caso contrário, tem apenas a origem
- `same-origin` - o referenciador enviado apenas ao carregar da mesma origem (porta, protocolo, domínio) no iframe
- `strict-origin` - envia a origem como referenciador se a página atual carregar via HTTPS e o iframe também carregar no protocolo HTTPS. Não envia nada se o iframe for carregado por HTTP
- `strict-origin-when-cross-origin` - envia a origem + caminho como referenciador ao trabalhar na mesma origem. Envia a origem como referenciador se a página atual for carregada por HTTPS e o iframe também for carregado no protocolo HTTPS. Não envia nada se o iframe for carregado por HTTP
- `unsafe-url` - envia a origem + caminho como referenciador mesmo ao carregar recursos de HTTP e a página atual é carregada por HTTPS
