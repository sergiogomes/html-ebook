# Multimedia tags: audio and video

I want to show you the `audio` and `video` tags in this section.

## The audio tag

This tag allows you to embed audio content in your HTML pages.
This element can stream audio, maybe using a microphone via `getUserMedia()`, or it can play an audio source that you reference using the `src` attribute:

```html
<audio src="file.mp3">
```

By default, the browser does not show any controls for this element. This means the audio will play only if set to autoplay (more on this later), and the user can't see how to stop it, control the volume, or move through the track.
To show the built-in controls, you can add the `controls` attribute:

```html
<audio src="file.mp3" controls>
```

Controls can have custom skin.

You can specify the MIME type of the audio file using the `type` attribute. If not set, the browser will try to determine it automatically:

```html
<audio src="file.mp3" controls type="audio/mpeg">
```

An audio file, by default, does not play automatically. Add the `autoplay` attribute to play the audio automatically:

```html
<audio src="file.mp3" controls autoplay>
```

> Note: mobile browsers don't allow autoplay

The `loop` attribute restarts the audio playing at 0:00 if set; otherwise, if not present, the audio stops at the end of the file:

```html
<audio src="file.mp3" controls autoplay loop>
```

You can also play an audio file muted using the `muted` attribute:

```html
<audio src="file.mp3" controls autoplay loop muted>
```

Using JavaScript, you can listen for various events happening on an `audio` element, the most basic of which are:

- `play` - when the audio file starts playing
- `pause` - when the audio file pauses from playing
- `playing` - when the audio file resumes from a pause
- `ended` - when the audio file reaches the end
