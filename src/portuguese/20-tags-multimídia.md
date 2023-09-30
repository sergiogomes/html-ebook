# Tags multimídia: áudio e vídeo

Quero mostrar as tags `audio` e `video` nesta seção.

## A tag de áudio

Esta tag permite incorporar conteúdo de áudio em suas páginas HTML.
Este elemento pode transmitir áudio, talvez usando um microfone via `getUserMedia()`, ou pode reproduzir uma fonte de áudio que você referencie usando o atributo `src`:

```html
<audio src="arquivo.mp3">
```

Por padrão, o navegador não mostra nenhum controle para este elemento. Isso significa que o áudio será reproduzido apenas se estiver configurado para reprodução automática (mais sobre isso mais tarde), e o usuário não consegue ver como interrompê-lo, controlar o volume ou percorrer a faixa.
Para mostrar os controles integrados, você pode adicionar o atributo `controls`:

```html
<audio src="arquivo.mp3" controls>
```

Os controles podem ter uma aparência personalizada.

Você pode especificar o tipo MIME do arquivo de áudio usando o atributo `type`. Se não for definido, o navegador tentará determiná-lo automaticamente:

```html
<audio src="arquivo.mp3" controls type="audio/mpeg">
```

Um arquivo de áudio, por padrão, não é reproduzido automaticamente. Adicione o atributo `autoplay` para reproduzir o áudio automaticamente:

```html
<audio src="arquivo.mp3" controls autoplay>
```

> Observação: navegadores de celular não permitem reprodução automática

O atributo `loop` reinicia a reprodução do áudio às 0:00 se definido; caso contrário, se não estiver presente, o áudio será interrompido no final do arquivo:

```html
<audio src="arquivo.mp3" controls autoplay loop>
```

Você também pode reproduzir um arquivo de áudio sem som usando o atributo `mute`:

```html
<audio src="arquivo.mp3" controls autoplay loop muted>
```

Usando JavaScript, você pode ouvir vários eventos acontecendo em um elemento `audio`, dos quais os mais básicos são:

- `play` - quando o arquivo de áudio começa a ser reproduzido
- `pause` - quando o arquivo de áudio faz uma pausa na reprodução
- `playing` - quando o arquivo de áudio recomeça de uma pausa
- `ended` - quando o arquivo de áudio chega ao fim

## A tag do vídeo

Esta tag permite incorporar conteúdo de vídeo em suas páginas HTML.
Este elemento pode transmitir vídeo usando uma webcam via `getUserMedia()` ou `WebRTC`, ou pode reproduzir uma fonte de vídeo que você referencie usando o atributo `src`:

```html
<video src="arquivo.mp4">
```

Por padrão, o navegador não mostra controles para este elemento, apenas o vídeo.
Isso significa que o vídeo será reproduzido apenas se estiver configurado para reprodução automática (mais sobre isso mais tarde), e o usuário não poderá ver como interrompê-lo, pausá-lo, controlar o volume ou pular para uma posição específica no vídeo.
Para mostrar os controles integrados, você pode adicionar o atributo `controls`:

```html
<video src="arquivo.mp4" controls>
```

Os controles podem ter uma aparência personalizada.
Você pode especificar o tipo MIME do arquivo de vídeo usando o atributo `type`. Se não for definido, o navegador tentará determiná-lo automaticamente:

```html
<video src="file.mp4" controls type="video/mp4">
```

Um arquivo de vídeo, por padrão, não é reproduzido automaticamente. Adicione o atributo `autoplay` para reproduzir o vídeo automaticamente:

```html
<video src="file.mp4" controls autoplay>
```

Alguns navegadores também exigem o atributo `mute` para reprodução automática. A reprodução automática do vídeo somente se estiver silenciado:

```html
<video src="file.mp4" controls autoplay muted>
```

O atributo `loop` reinicia a reprodução do vídeo às 0:00 se definido; caso contrário, se não estiver presente, o vídeo para no final do arquivo:

```html
<video src="file.mp4" controls autoplay loop>
```

Você pode definir uma imagem para ser a imagem do `poster`:

```html
<video src="file.mp4" poster="picture.png">
```

Se não estiver presente, o navegador exibirá o primeiro quadro do vídeo assim que estiver disponível.

Você pode definir os atributos `width` e `height` para definir o espaço que o elemento ocupará para que o navegador possa considerá-lo e não altere o layout quando for finalmente carregado. Leva um valor numérico expresso em pixels.

Usando JavaScript, você pode ouvir vários eventos acontecendo em um elemento `video`, sendo os mais básicos:

- `play` - quando o arquivo de vídeo começa a ser reproduzido
- `pause` - quando o arquivo de vídeo faz uma pausa na reprodução
- `playing` - quando o arquivo de vídeo retoma de uma pausa
- `ended` - quando o final do arquivo de vídeo chegou ao fim
