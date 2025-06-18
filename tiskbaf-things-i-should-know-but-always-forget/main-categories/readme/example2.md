# To get a list of the dependencies of a package

```
sudo apt show <package>
```

Example output of `sudo apt show vlc`:

```
Package: vlc
Version: 3.0.17.4-3
Priority: optional
Section: video
Maintainer: Debian Multimedia Maintainers <debian-multimedia@lists.debian.org>
Installed-Size: 237 kB
Provides: mp3-decoder
Depends: vlc-bin (= 3.0.17.4-3), vlc-plugin-base (= 3.0.17.4-3), vlc-plugin-qt (= 3.0.17.4-3), vlc-plugin-video-output (= 3.0.17.4-3)
Recommends: vlc-l10n (= 3.0.17.4-3), vlc-plugin-access-extra (= 3.0.17.4-3), vlc-plugin-notify (= 3.0.17.4-3), vlc-plugin-samba (= 3.0.17.4-3), vlc-plugin-skins2 (= 3.0.17.4-3), vlc-plugin-video-splitter (= 3.0.17.4-3), vlc-plugin-visualization (= 3.0.17.4-3)
Suggests: vlc-plugin-fluidsynth (= 3.0.17.4-3), vlc-plugin-jack (= 3.0.17.4-3), vlc-plugin-pipewire, vlc-plugin-svg (= 3.0.17.4-3)
Homepage: <https://www.videolan.org/vlc/>
Tag: hardware::storage, hardware::storage:cd, hardware::storage:dvd,
 hardware::video, implemented-in::c, implemented-in::c++,
 interface::commandline, interface::graphical, interface::x11,
 protocol::ipv6, protocol::ssl, role::program, scope::application,
 scope::utility, sound::compression, sound::player, uitoolkit::ncurses,
 uitoolkit::qt, use::converting, use::playing, works-with-format::TODO,
 works-with-format::mp3, works-with-format::oggtheora,
 works-with-format::oggvorbis, works-with-format::wav, works-with::TODO,
 works-with::audio, works-with::video, x11::application
Download-Size: 146 kB
APT-Sources: <http://http.kali.org/kali> kali-rolling/main amd64 Packages
Description: multimedia player and streamer
 VLC is the VideoLAN project's media player. It plays MPEG, MPEG-2, MPEG-4,
 DivX, MOV, WMV, QuickTime, WebM, FLAC, MP3, Ogg/Vorbis files, DVDs, VCDs,
 podcasts, and multimedia streams from various network sources.
 .
 VLC can also be used as a streaming server that duplicates the stream it
 reads and multicasts them through the network to other clients, or serves
 them through HTTP.
 .
 VLC has support for on-the-fly transcoding of audio and video formats, either
 for broadcasting purposes or for movie format transformations. Support for
 most output methods is provided by this package, but features can be added by
 installing additional plugins:
  * vlc-plugin-access-extra
  * vlc-plugin-fluidsynth
  * vlc-plugin-jack
  * vlc-plugin-notify
  * vlc-plugin-samba
  * vlc-plugin-skins2
  * vlc-plugin-svg
  * vlc-plugin-video-splitter
  * vlc-plugin-visualization
```
