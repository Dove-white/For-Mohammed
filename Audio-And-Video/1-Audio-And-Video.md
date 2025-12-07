## 🎧 Audio & Video in HTML

Modern web pages can natively play audio and video without relying on plugins like Flash. HTML provides two powerful elements — `<audio>` and `<video>` — that make embedding media simple, while also allowing extra functionality like controls, autoplay, looping, and more.

---

## Embedding Video

### 🖥️ Basic Video Tag

To embed a video in your page, you use the `<video>` element. Here’s a simple example:

```html
<video src="rabbit320.webm" controls>
  <p>Your browser doesn't support HTML video. Here is a
    <a href="rabbit320.webm">link to the video</a> instead.
  </p>
</video>
```

- `src`: Specifies the video file.
- `controls`: Adds the browser’s default playback interface (play/pause, volume, etc).
- The `<p>` inside is fallback content — shown when the browser doesn't support `<video>`.

![My Image](image/video-player-UI.png "Optional title")
<!-- ![My Image](./1-Frontend-Development/1-HTML/3-Images-Media-And-File-Paths/2-Audio-And-Video/image/video-player-UI.png "Optional title") -->

### 📁 Multiple Sources for Compatibility

Different browsers support different video formats (containers and codecs). To ensure your video works everywhere, provide multiple sources inside `<video>`:

```html
<video controls>
  <source src="rabbit320.mp4" type="video/mp4" />
  <source src="rabbit320.webm" type="video/webm" />
  <p>Your browser doesn't support this video. Here is a
    <a href="rabbit320.mp4">link to the video</a> instead.
  </p>
</video>
```

- `<source>` elements let the browser pick the first format it can play.
- `type` (MIME type) helps the browser skip unsupported formats faster.

### 🎛️ Controls & Autoplay (and More)

You can add more attributes to control how the video behaves:

```html
<video
  controls
  width="400"
  height="400"
  autoplay
  loop
  muted
  preload="auto"
  poster="poster.png">
  
  <source src="rabbit320.mp4" type="video/mp4" />
  <source src="rabbit320.webm" type="video/webm" />
  
  <p>Your browser doesn't support this video. Here is a
    <a href="rabbit320.mp4">link to the video</a> instead.
  </p>
</video>
```

- `width` & `height`: Size of the video player (or control via CSS).
- `autoplay`: Starts playback as soon as possible (use sparingly).
- `loop`: Replays the video automatically when it ends.
- `muted`: Starts with the sound off.
- `preload`: How much of the video to buffer in advance.
- `poster`: Image shown before the video plays.

![My Image](image/poster-image.png "Optional title")
<!-- ![My Image](./1-Frontend-Development/1-HTML/3-Images-Media-And-File-Paths/2-Audio-And-Video/image/poster-image.png "Optional title") -->

---

## Embedding Audio

### 🎵 Basic Audio Tag

Embedding audio is very similar to video. Use the `<audio>` element:

```html
<audio controls>
  <source src="viper.mp3" type="audio/mp3" />
  <source src="viper.ogg" type="audio/ogg" />
  <p>Your browser doesn't support this audio file. Here is a
    <a href="viper.mp3">link to the audio</a> instead.
  </p>
</audio>
```

- `controls` adds play/pause, volume, and progress bar.
- Fallback `<p>` offers a link if audio isn’t supported.

### 🔁 Controls & Autoplay in Audio

Just like video, `<audio>` supports attributes like:
- `autoplay`
- `loop`
- `muted`
- `preload` ("none", "metadata", "auto")

---

## Controls and Autoplay — Why They Matter

- **Controls**: Essential for accessibility. Users need a way to play, pause, adjust volume, and stop media.
- **Autoplay**: Can be useful, but often frowned upon. Forces media on users, can annoy them, and increase data usage.

---

## Putting It All Together: Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Media Example</title>
</head>
<body>

  <h1>Welcome to My Media Page</h1>

  <video
    controls
    width="480"
    poster="poster.png"
    loop
    muted
    preload="auto">
    
    <source src="rabbit320.mp4" type="video/mp4" />
    <source src="rabbit320.webm" type="video/webm" />
    
    <p>Your browser doesn’t support video.
      <a href="rabbit320.mp4">Download the video instead.</a>
    </p>
  </video>

  <audio controls autoplay preload="auto">
    <source src="viper.mp3" type="audio/mp3" />
    <source src="viper.ogg" type="audio/ogg" />
    <p>Your browser doesn’t support audio.
      <a href="viper.mp3">Download the audio instead.</a>
    </p>
  </audio>

</body>
</html>
```

---

## Why Use These Native Elements?

- 💡 **Performance & Accessibility**: Native elements are faster and more accessible.
- 🌍 **Browser Compatibility**: Offering multiple sources ensures playback across browsers.
- ♿ **User Control**: Controls help users manage playback and volume.

