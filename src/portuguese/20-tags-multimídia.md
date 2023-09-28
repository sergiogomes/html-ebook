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
