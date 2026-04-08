# Release notes — 0.0.24

Release date: 23-Feb-2026

## English

### New features and improvements
- **Tap-to-play setting:** Choose between single tap or double tap to start playback from Settings. Double tap remains the default to prevent accidental starts.
- **Auto-restart finished books:** When you play a book you've already finished (at 100%), it now automatically restarts from the beginning instead of resuming at the last track's end.
- **Native sort for local files:** New "Default" sort option shows local files and folders in their natural order from your device, rather than forcing a specific sort.
- **Duration in library:** Book duration is now displayed directly in the library list for supported sources.
- **Optimized playback buffers:** Reduced memory usage and faster recovery after network hiccups. Buffer targets adjusted from 2 minutes down to 40 seconds max, with quicker rebuffer thresholds.
- **More reliable loudness normalization:** The app now handles audio effect compatibility issues gracefully on devices where loudness enhancement may crash.
- **Single audio file support:** Individual audio files (MP3, M4A, M4B, FLAC, WAV) in local folders now correctly save and restore playback position and metadata.
- **Consistent torrent/magnet handling:** Books added from .torrent files now use the same identifier as their magnet link equivalents, ensuring consistent playback history and favorites across both methods.

### Bug fixes
- Fixed crashes when loudness normalization encountered invalid audio sessions.
- Fixed metadata not persisting for single audio files selected via SAF.
- Fixed parsing errors on certain content source detail pages.
- Fixed potential crashes from malformed selector patterns.

### Behavior changes
- Default sort for local files changed from "Recent" to "Default" (native folder order).
- Buffer thresholds adjusted: "Good" state now requires 6 seconds buffered (was 1.8s), "Excellent" requires 20 seconds (was 60s).

### BREAKING CHANGES
None

### Risks / What to test
- Single/double tap playback start setting works correctly
- Finished books auto-restart when played again
- Local file browsing with "Default" sort
- Playback position saves and restores for single audio files
- Loudness normalization toggle works without crashes
- Buffering behavior during poor network conditions

---

## Русский

### Новые возможности и улучшения
- **Настройка запуска воспроизведения:** Выберите одинарное или двойное нажатие для запуска воспроизведения в Настройках. Двойное нажатие остаётся по умолчанию для предотвращения случайных запусков.
- **Автоперезапуск прослушанных книг:** При воспроизведении книги, которую вы уже завершили (на 100%), она автоматически начинается сначала вместо возобновления в конце последней главы.
- **Родная сортировка локальных файлов:** Новый пункт «По умолчанию» показывает локальные файлы и папки в их естественном порядке с устройства, без принудительной сортировки.
- **Длительность в библиотеке:** Длительность книги теперь отображается прямо в списке библиотеки для поддерживаемых источников.
- **Оптимизированные буферы воспроизведения:** Снижено использование памяти и ускорено восстановление после сетевых проблем. Максимальный буфер уменьшен с 2 минут до 40 секунд, с более быстрыми порогами восстановления.
- **Более надёжная нормализация громкости:** Приложение теперь корректно обрабатывает проблемы совместимости аудиоэффектов на устройствах, где усиление громкости может вызывать сбои.
- **Поддержка отдельных аудиофайлов:** Отдельные аудиофайлы (MP3, M4A, M4B, FLAC, WAV) в локальных папках теперь корректно сохраняют и восстанавливают позицию воспроизведения и метаданные.
- **Согласованная обработка торрентов и магнит-ссылок:** Книги, добавленные из .torrent-файлов, теперь используют тот же идентификатор, что и их аналоги с магнит-ссылками, обеспечивая единообразие истории воспроизведения и избранного.

### Исправления ошибок
- Исправлены сбои при нормализации громкости с недействительными аудиосессиями.
- Исправлено несохранение метаданных для отдельных аудиофайлов, выбранных через SAF.
- Исправлены ошибки разбора на страницах деталей некоторых источников контента.
- Исправлены потенциальные сбои от некорректных паттернов селекторов.

### Изменения поведения
- Сортировка по умолчанию для локальных файлов изменена с «Недавние» на «По умолчанию» (родной порядок папки).
- Пороги буферизации настроены: состояние «Хорошо» теперь требует 6 секунд буфера (было 1.8с), «Отлично» требует 20 секунд (было 60с).

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
Нет

### Риски / Что тестировать
- Настройка одинарного/двойного нажатия для запуска воспроизведения работает корректно
- Прослушанные книги автоматически перезапускаются при повторном воспроизведении
- Просмотр локальных файлов с сортировкой «По умолчанию»
- Позиция воспроизведения сохраняется и восстанавливается для отдельных аудиофайлов
- Переключатель нормализации громкости работает без сбоев
- Поведение буферизации при плохих сетевых условиях
