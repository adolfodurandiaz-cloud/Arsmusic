# armusic (Android)

Minimalist offline music player project, built with Kotlin and AndroidX Media3.

## Included in this starter
- Scans the device's local music library through MediaStore.
- Plays local audio through Media3 ExoPlayer.
- Background playback through a `MediaSessionService` with Android media notification controls.
- Play/pause, previous/next, shuffle and repeat.
- Embedded artwork display when supplied by the audio metadata.
- Android audio effect Equalizer controls where supported by the device/output.
- Sleep timer: 15, 30, 45 or 60 minutes.
- Synchronized lyrics from `.lrc` files matching the audio filename.

## Build the APK
1. Install Android Studio (current stable) and its Android SDK (API 35 recommended).
2. Open this folder in Android Studio.
3. Let Gradle sync and download dependencies.
4. Connect an Android device with USB debugging enabled, or create an emulator.
5. Use **Build > Build APK(s)**. Android Studio will show the generated APK location.

The project has not been built in this environment because an Android SDK/Gradle installation is not available here. Treat this as a starter implementation that should be compiled and tested in Android Studio before daily use.

## Lyrics
Place a UTF-8 `.lrc` file beside the audio file and give it the same base filename, for example:
- `Cancion.mp3`
- `Cancion.lrc`

Example LRC:
```text
[00:00.00]Primera línea
[00:05.20]Segunda línea
[00:09.50]Tercera línea
```

## Notes and next steps
- The app requests permission to read audio files. It does not upload or stream your music.
- Some Android manufacturers restrict equalizer effects or expose them only for certain audio routes.
- Android 13+ uses `READ_MEDIA_AUDIO`; older Android versions use `READ_EXTERNAL_STORAGE`.
- A polished follow-up can add album/artist filters, playlists, persistent preferences, richer artwork extraction, accessibility review and automated device tests.
