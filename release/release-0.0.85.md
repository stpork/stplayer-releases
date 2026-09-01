# Release notes — 0.0.85

Release date: 02-Sep-2026

## English

- Added audio playback from local MP4, MKV, WebM, AVI, and MOV files.
- Improved playback reliability for YouTube streams and modern playlists.
- Failed or interrupted downloads are now preserved for recovery instead of being removed.
- Incomplete or inaccessible downloads are safely blocked from playback, preventing partial or invalid content from opening.
- Improved recovery of library data, bookmarks, playback progress, and download information after interruptions or unexpected shutdowns.
- Improved synchronization reliability, preventing partial group joins and restoring the freshest playback position.
- Saved settings are now loaded more reliably during app startup, including on slower devices.

### Behavior changes

- Supported local video files appear as playable audio.
- Recoverable downloads remain available for retry or resume.
- Downloads with inaccessible storage are not substituted for online content until access is restored.

### BREAKING CHANGES

None

### Risks / What to test

- Scan and play supported local video files.
- Browse and play YouTube playlists.
- Interrupt and resume regular and torrent downloads.
- Revoke and restore access to the download location.
- Verify playback progress and settings after restart and synchronization.

## Русский

- Добавлено воспроизведение звука из локальных файлов MP4, MKV, WebM, AVI и MOV.
- Повышена надёжность воспроизведения потоков и современных плейлистов YouTube.
- Неудачные или прерванные загрузки теперь сохраняются для восстановления, а не удаляются.
- Незавершённые или недоступные загрузки безопасно блокируются, чтобы исключить воспроизведение неполных или повреждённых данных.
- Улучшено восстановление библиотеки, закладок, позиции воспроизведения и сведений о загрузках после сбоев или неожиданного завершения приложения.
- Повышена надёжность синхронизации: исключено частичное присоединение к группе и восстанавливается самая свежая позиция воспроизведения.
- Сохранённые настройки теперь надёжнее загружаются при запуске приложения, в том числе на медленных устройствах.

### Изменения поведения

- Поддерживаемые локальные видеофайлы отображаются как аудио и доступны для воспроизведения.
- Загрузки, которые можно восстановить, сохраняются для повторной попытки или продолжения.
- Загрузки в недоступном хранилище не заменяют онлайн-версию до восстановления доступа.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ

Нет

### Риски / Что проверить

- Сканирование и воспроизведение поддерживаемых локальных видеофайлов.
- Просмотр и воспроизведение плейлистов YouTube.
- Прерывание и возобновление обычных и торрент-загрузок.
- Отзыв и повторное предоставление доступа к папке загрузок.
- Сохранение позиции воспроизведения и настроек после перезапуска и синхронизации.