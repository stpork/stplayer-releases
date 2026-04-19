# Release notes — 0.0.54

Release date: 20-Apr-2026

## English
- Improved background battery usage: the app now wakes up less often when playback is paused or when there are no active torrents.
- Fixed playback control glitches where pause/play/seek commands could be silently dropped under heavy activity — transport controls are now more reliable.
- Android 15: proper edge-to-edge display support for a cleaner full-screen look and correct insets.
- More reliable playback on titles with multiple audio dubs (consistent dub ordering) and smoother re-engagement after a book finishes.
- Strengthened security of the in-app cover artwork provider against malformed external requests.
- Minor locale/text polish across supported languages.
- General stability improvements in player state handling and track-end transitions.

### Behavior changes
- Android 15 devices now render the app edge-to-edge; system bars overlay content with correct padding.
- When no torrents are active, the torrent engine is fully paused to save battery.

### BREAKING CHANGES
- None

### Risks / What to test
- Playback start/pause/resume, seek, and next/previous across local, SAF, web, downloaded, and torrent sources.
- Background playback and notification controls; Android Auto and Bluetooth/headset media buttons.
- Cold start, resume after app kill, and session restore.
- BYT source: books with multiple audio dubs; end-of-book transition and re-engagement.
- Android 15: edge-to-edge layout, status/navigation bar insets, rotation.
- Battery behavior during long paused sessions and with no torrents active.
- Cover artwork display in notification, lock screen, and Android Auto.

## Русский
- Снижено энергопотребление в фоне: приложение реже «просыпается» при паузе и когда нет активных торрентов.
- Исправлены сбои управления воспроизведением, при которых команды пауза/воспроизведение/перемотка могли теряться под нагрузкой — транспортные кнопки работают надёжнее.
- Android 15: полноценная поддержка режима «от края до края» с корректными отступами.
- Более стабильное воспроизведение книг с несколькими озвучками (стабильный порядок дубляжей) и плавное возобновление после завершения книги.
- Усилена защита внутреннего провайдера обложек от некорректных внешних запросов.
- Мелкие улучшения локализаций.
- Общая стабильность состояния плеера и переходов между треками.

### Изменения поведения
- На устройствах с Android 15 интерфейс отображается «от края до края» с правильными отступами для системных панелей.
- При отсутствии активных торрентов торрент-движок полностью приостанавливается для экономии батареи.

### BREAKING CHANGES
- Нет

### Риски / Что протестировать
- Запуск, пауза, возобновление, перемотка, переключение треков на источниках: локальный, SAF, веб, загруженное, торрент.
- Фоновое воспроизведение и управление из уведомления; Android Auto и кнопки Bluetooth/гарнитуры.
- Холодный старт, восстановление после завершения процесса, восстановление сессии.
- Источник BYT: книги с несколькими озвучками; завершение книги и повторный запуск.
- Android 15: раскладка «от края до края», отступы системных панелей, поворот экрана.
- Расход батареи при длительной паузе и без активных торрентов.
- Отображение обложек в уведомлении, на экране блокировки и в Android Auto.
