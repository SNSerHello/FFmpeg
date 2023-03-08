FFmpeg README
=============

## Install 3rd-party libraries

```bash
git clone --recursive https://github.com/FFmpeg/nv-codec-headers.git
cd nv-codec-headers
sudo make install

sudo apt install \
  nasm \
  yasm \
  libchromaprint-dev \
  libfrei0r-ocaml-dev \
  libgnutls28-dev \
  libladspa-ocaml-dev \
  liblilv-dev \
  libass-dev \
  libbluray-dev \
  libbs2b-dev \
  libcaca-dev \
  libcodec2-dev \
  libdc1394-22-dev \
  libdrm-dev \
  libgme-dev \
  libgsm1-dev \
  libmysofa-dev \
  libopenjp2-7-dev \
  libopenmpt-dev \
  libopus-dev \
  libpulse-dev \
  librsvg2-dev \
  librubberband-dev \
  libshine-dev \
  libsnappy-dev \
  libsoxr-dev \
  libssh-dev \
  libspeex-dev \
  libtheora-dev \
  libtwolame-dev \
  libvidstab-dev \
  libvpx-dev \
  libwebp-dev \
  libx264-dev \
  libx265-dev \
  libxvidcore-dev \
  libzmq3-dev \
  libzvbi-dev \
  libopenal-dev \
  libomxil-bellagio-dev \
  libjack-dev \
  libcdio-dev \
  libcdio-cdda-dev \
  libcdio-paranoia-dev \
  libffmpeg-nvenc-dev \
  libsdl2-dev
```

## Build FFmpeg

```bash
./configure \
  --prefix=./dist \
  --extra-version=0ubuntu0.1 \
  --toolchain=hardened \
  --arch=amd64 \
  --enable-gpl \
  --disable-stripping \
  --disable-filter=resample \
  --enable-gnutls \
  --enable-ladspa \
  --enable-libaom \
  --enable-libass \
  --enable-libbluray \
  --enable-libbs2b \
  --enable-libcaca \
  --enable-libcdio \
  --enable-libcodec2 \
  --enable-libfontconfig \
  --enable-libfreetype \
  --enable-libfribidi \
  --enable-libgme \
  --enable-libgsm \
  --enable-libjack \
  --enable-libmp3lame \
  --enable-libmysofa \
  --enable-libopenjpeg \
  --enable-libopenmpt \
  --enable-libopus \
  --enable-libpulse \
  --enable-librsvg \
  --enable-librubberband \
  --enable-libshine \
  --enable-libsnappy \
  --enable-libsoxr \
  --enable-libspeex \
  --enable-libssh \
  --enable-libtheora \
  --enable-libtwolame \
  --enable-libvidstab \
  --enable-libvorbis \
  --enable-libvpx \
  --enable-libwebp \
  --enable-libx265 \
  --enable-libxml2 \
  --enable-libxvid \
  --enable-libzmq \
  --enable-libzvbi \
  --enable-lv2 \
  --enable-omx \
  --enable-openal \
  --enable-opencl \
  --enable-opengl \
  --enable-sdl2 \
  --enable-libdc1394 \
  --enable-libdrm \
  --enable-nvenc \
  --enable-chromaprint \
  --enable-frei0r \
  --enable-libx264 \
  --enable-shared \
  && make install -j
```

FFmpeg is a collection of libraries and tools to process multimedia content
such as audio, video, subtitles and related metadata.

## Libraries

* `libavcodec` provides implementation of a wider range of codecs.
* `libavformat` implements streaming protocols, container formats and basic I/O access.
* `libavutil` includes hashers, decompressors and miscellaneous utility functions.
* `libavfilter` provides means to alter decoded audio and video through a directed graph of connected filters.
* `libavdevice` provides an abstraction to access capture and playback devices.
* `libswresample` implements audio mixing and resampling routines.
* `libswscale` implements color conversion and scaling routines.

## Tools

* [ffmpeg](https://ffmpeg.org/ffmpeg.html) is a command line toolbox to
  manipulate, convert and stream multimedia content.
* [ffplay](https://ffmpeg.org/ffplay.html) is a minimalistic multimedia player.
* [ffprobe](https://ffmpeg.org/ffprobe.html) is a simple analysis tool to inspect
  multimedia content.
* Additional small tools such as `aviocat`, `ismindex` and `qt-faststart`.

## Documentation

The offline documentation is available in the **doc/** directory.

The online documentation is available in the main [website](https://ffmpeg.org)
and in the [wiki](https://trac.ffmpeg.org).

### Examples

Coding examples are available in the **doc/examples** directory.

## License

FFmpeg codebase is mainly LGPL-licensed with optional components licensed under
GPL. Please refer to the LICENSE file for detailed information.

## Contributing

Patches should be submitted to the ffmpeg-devel mailing list using
`git format-patch` or `git send-email`. Github pull requests should be
avoided because they are not part of our review process and will be ignored.
