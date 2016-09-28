# champ

[![Codewake](https://www.codewake.com/badges/ask_question_flat_square.svg)](https://www.codewake.com/p/champ)

Experiment into 2nd screen player for Plex protocol on single board
computers like RPi. Build instructions https://github.com/dz0ny/champ/wiki/Building-for-RPi

## Developing

1. Install local build of mpv and ffmpeg (https://github.com/mpv-player/mpv-build#instructions-for-debian-and-ubuntu) and use  ffmpeg_options and mpv_options specified below.
2. Set HOPATH to root of the project or use gobu
3. make

### ffmpeg_options
```
--enable-pic
--enable-gpl
--enable-libfreetype
--enable-libmp3lame
--enable-libopus
--enable-libtheora
--enable-libvorbis
--enable-libvpx
--enable-gnutls
--enable-libx264
--enable-libx265
--enable-nonfree
--disable-encoders
--disable-muxers
--disable-indevs
--disable-ffplay
--disable-ffprobe
--disable-ffmpeg
--disable-ffserver
--disable-debug
--disable-doc
```

### mpv_options
```
--prefix=/
--enable-libmpv-shared
--disable-tv
--disable-dvbin
--disable-libbluray
--disable-dvdread
--disable-cdda
--disable-cplayer
--disable-debug-build
--disable-manpage-build
--disable-html-build
--disable-pdf-build
```

## Install

App is packaged with snap and published in app store and under https://github.com/dz0ny/champ/releases

## Usage

The main thing
```
➜ champ [<flags>]

Minimalistic Plex 2nd screen client

Flags:
  --help                  Show context-sensitive help (also try --help-long and
                          --help-man).
  --debug                 Verbose mode.
  --title="Champ Player"  Name of this player
  --port="32016"          HTTP server port
  --version               Show application version.
```

Dev helper for MPV integration, this will later be integration into champ.
```
➜ spinwheel [<flags>]

Shuffle player which also plays from YouTube(tm)

Flags:
      --help               Show context-sensitive help (also try --help-long and --help-man).
      --debug              Verbose mode.
  -p, --playlist=PLAYLIST  Path to playlist file (.yaml)
      --version            Show application version.

```
