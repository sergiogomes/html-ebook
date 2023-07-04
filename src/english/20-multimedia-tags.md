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

## The video tag

This tag allows you to embed video content in your HTML pages.
This element can stream video using a webcam via `getUserMedia()` or `WebRTC`, or it can play a video source that you reference using the `src` attribute:

```html
<video src="file.mp4">
```

By default, the browser does not show controls for this element, just the video.
This means the video will play only if set to autoplay (more on this later), and the user can't see how to stop it, pause it, control the volume, or skip to a specific position in the video.
To show the built-in controls, you can add the `controls` attribute:

```html
<video src="file.mp4" controls>
```

Controls can have custom skin.
You can specify the MIME type of the video file using the `type` attribute. If not set, the browser will try to determine it automatically:

```html
<video src="file.mp4" controls type="video/mp4">
```

A video file, by default, does not play automatically. Add the `autoplay` attribute to play the video automatically:

```html
<video src="file.mp4" controls autoplay>
```

Some browsers also require the `muted` attribute to autoplay. The video autoplay only if muted:

```html
<video src="file.mp4" controls autoplay muted>
```

The `loop` attribute restarts the video playing at 0:00 if set; otherwise, if not present, the video stops at the end of the file:

```html
<video src="file.mp4" controls autoplay loop>
```

You can set an image to be the `poster` image:

```html
<video src="file.mp4" poster="picture.png">
```

If not present, the browser will display the first frame of the video as soon as it's available.

You can set the `width` and `height` attributes to set the space that the element will take so that the browser can account for it and it does not change the layout when it's finally loaded. It takes a numeric value expressed in pixels.

Using JavaScript, you can listen for various events happening on a `video` element, the most basic of which are:

- `play` - when the video file starts playing
- `pause` - when the video file pauses from playing
- `playing` - when the video file resumes from a pause
- `ended` - when the video file end of the video file reached the end
