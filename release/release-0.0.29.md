# Release notes — 0.0.29

Release date: 03-Mar-2026 

## English
- Added playback pitch control in the player, with fine-step adjustment and quick reset to normal voice.
- Improved resume reliability when reopening books from History, including a fallback to saved player state when a direct resume point is missing.
- Fixed a resume regression where playback could jump back to `0:00` right after restore.
- Improved torrent playback startup by reducing blocking during initial buffering, which helps playback begin more reliably.
- Added clearer torrent error handling for invalid sources/files and timeout scenarios.
- Improved source availability with mirror-aware fetching and matching, including mirror support for RuTracker.
- Improved Library navigation state handling so list behavior is more stable across source/category/search contexts.
- Refined History card layout consistency and metadata readability.
- Improved duration display on the book screen to use precise `HH:MM:SS` formatting when valid duration data is available.
- Improved media title formatting for external clients (such as car and Bluetooth surfaces) in single-track cases.

### Behavior changes
- You can now adjust playback pitch separately from playback speed.
- Resume from History now has a stronger fallback path and is less likely to restart from the wrong position.
- Source loading can now fall back to configured mirrors when the primary site is unavailable.
- Book duration display may now be hidden instead of showing imprecise text when valid duration cannot be resolved.

### BREAKING CHANGES
- None

### Risks / What to test
- Verify pitch adjustment during active playback, including reset behavior.
- Resume several books from History (single-track and multi-track) and confirm position accuracy.
- Test RuTracker browsing/playback when the primary domain is slow or unavailable.
- Start torrent playback on weak/slow peers and confirm startup reliability and error messages.
- Check Library state continuity when switching between source lists, categories, and search.

## Русский
- Добавлено управление тоном воспроизведения в плеере с точной пошаговой настройкой и быстрым сбросом к обычному голосу.
- Повышена надёжность возобновления при открытии книг из Истории, включая запасной сценарий через сохранённое состояние плеера, если прямой точки продолжения нет.
- Исправлена регрессия возобновления, из-за которой воспроизведение могло сбрасываться на `0:00` сразу после восстановления.
- Улучшен запуск воспроизведения торрентов за счёт уменьшения блокировок на этапе начальной буферизации, что повышает вероятность успешного старта.
- Добавлена более понятная обработка ошибок торрентов для невалидных источников/файлов и сценариев таймаута.
- Повышена доступность источников за счёт mirror-aware загрузки и сопоставления, включая поддержку зеркала для RuTracker.
- Улучшена обработка состояния навигации в Библиотеке: поведение списков стало стабильнее между режимами источник/категория/поиск.
- Улучшена визуальная стабильность карточек Истории и читаемость метаданных.
- Улучшено отображение длительности на экране книги: теперь используется точный формат `HH:MM:SS`, если доступны корректные данные.
- Улучшено форматирование заголовков для внешних клиентов (например, авто и Bluetooth) в сценариях с одной дорожкой.

### Behavior changes
- Теперь можно настраивать тон воспроизведения отдельно от скорости.
- Возобновление из Истории получило более надёжный запасной путь и реже стартует с неверной позиции.
- Загрузка источников теперь может переключаться на настроенные зеркала, если основной сайт недоступен.
- Длительность книги теперь может скрываться вместо показа неточного текста, если корректно определить её не удалось.

### BREAKING CHANGES
- None

### Risks / What to test
- Проверьте настройку тона во время активного воспроизведения, включая сброс.
- Откройте несколько книг из Истории (с одной и несколькими дорожками) и проверьте точность позиции.
- Проверьте просмотр/воспроизведение RuTracker, когда основной домен медленный или недоступен.
- Запустите воспроизведение торрента на слабых/медленных пирах и проверьте надёжность старта и тексты ошибок.
- Проверьте сохранение состояния Библиотеки при переключении между списками источников, категориями и поиском.