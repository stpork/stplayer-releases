# STPlayer — Stream Transport Player
An Android audiobook player with built-in access to online catalogs, local media, and torrent sources.

## Installation
Download the latest `.apk` from the [Releases](../../releases) page and install it on your device.

> **Android 8.0 or newer required.**
> You may need to allow installation from unknown sources in your device settings (*Settings → Apps → Special app access → Install unknown apps*).

## Features

### Playback
- Adjustable playback speed and pitch
- Sleep timer — fixed duration, end-of-track, scheduled, or motion-reset (stops when you stop moving)
- Skip silence — automatically skips silent gaps
- Loudness normalization
- 30-second skip forward and backward
- Bookmarks with custom icons and timestamps
- Multi-track book support with track picker
- Configurable playback start: always resume, last device used, headset/Bluetooth only, or never auto-start
- Single-tap or double-tap to play

### Library
- Playback history with search
- Favorites — books, genres, authors, and performers
- Per-source browsing: genres, authors, narrators, collections
- Sorting by: newest, popular, rating, trending, discussed — by day, week, month, or all time
- Search within sources

### Downloads
- Download audiobooks for offline playback
- Configurable download folder (any location you choose)
- Adjustable concurrent download limits
- Download progress tracking

### Local Media
- Browse audio files from any folder on your device
- Supports MP3, M4A, M4B with embedded cover art
- Torrent playback (magnet links and .torrent files)

### Android Auto
- Full Android Auto support: history, favorites, sources, and search

### Appearance
- Light, Dark, System, and Twilight themes
- Three UI scale options (Small, Medium, Large)
- 12 interface languages: English, Russian, German, French, Spanish, Dutch, Finnish, Portuguese, Swedish, Turkish, Chinese, Japanese

## Built-in Sources
The app includes several built-in audiobook catalogs. No account is needed for the free sources.

| Source | Content | Language |
|--------|---------|----------|
| **LibriVox** | Public domain audiobooks | Multi-language |
| **LoyalBooks** | Public domain audiobooks — Top 100 and genre browsing | English |
| **Digitalbook.io** | Free audiobook catalog | Multi-language |
| **Bibe** | Classic audiobooks | Russian |
| **Local Library** | Audio files from device storage, downloads, and torrents | Any |

### Extended Catalog
Users with access to the extended catalog get additional sources, including a large selection of Russian-language audiobook sites and YouTube. Extended catalog sources are loaded automatically from `Android/media/com.st.player/sources/` — place your subscription source files there and the app picks them up on next launch.

## Permissions
| Permission | Why |
|-----------|-----|
| Internet | Browse and stream online audiobook sources |
| Access network state | Detect connectivity before attempting network requests |
| Foreground service | Keep playback running while the screen is off |
| Wake lock | Prevent the CPU from sleeping during active playback |
| Post notifications | Show the playback notification and controls |
| Read audio files | Access local audio files for playback |
| Vibrate | Optional haptic feedback on playback control gestures |

The app does not access your location, contacts, microphone, or camera.

## Privacy
The app uses Google Firebase for crash reporting and performance monitoring, and communicates with the audiobook sources you browse. No personal data is collected by the developer.

See the full [Privacy Policy](docs/index.md).

## License
© 2025–2026 stpork. All rights reserved.
Personal use only. See [LICENSE](LICENSE) for terms.
