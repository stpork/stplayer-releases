# Release notes — 0.0.55

Release date: 23-Apr-2026

## English
- History and Favorites now keep a built-in display cache, so titles, authors, performers, cover art and duration stay visible even after a reinstall or "Clear data".
- When book metadata is temporarily unavailable, entries show a human-readable fallback title (e.g. YouTube video ID or a cleaned-up path name) instead of a raw identifier.
- Fixed a rare issue where a phantom/ghost entry could appear after certain state transitions.
- Fixed playback on primary-storage folders (Media/Music/Documents) on Android 11+: files that previously failed with permission errors now play reliably via a SAF fallback, and position tracking is preserved.
- Fixed rare UI freezes caused by settings being written synchronously on the main thread under heavy write load; writes are now non-blocking.
- Expanded catalog support for the RTR provider, including a wider set of categories and listings.
- More reliable saving of the stp.lib library file: stale temporary files no longer block history/favorites from being written, and write failures are logged with clearer reasons.
- Request handling improvements for web sources: more resilient retries and tuned timeouts for RTR, reducing transient loading failures.
- More consistent merging of book metadata across scrapes, avoiding unnecessary overwrites and reducing flicker of details (performer/genre/description) on second-pass refresh.
- New in-app file logging for non-release builds: a rolling 7-day log is saved to the app's external files folder to help with diagnosing issues.
- Translations refreshed across all supported languages (DE, ES, FI, FR, JA, NL, PT, RU, SV, TR, ZH).

### Behavior changes
- History/Favorites list now renders immediately from the stp.lib cache and falls back to per-book metadata only when needed; the per-book store remains the source of truth for details.
- Preference commits triggered on the main thread are automatically degraded to asynchronous writes to prevent UI jank.

### BREAKING CHANGES
- None

### Risks / What to test
- Upgrade path: existing 0.0.54 history/favorites still load and are re-saved in the new format.
- Downgrade to 0.0.54 is not supported — verify user expectation.
- Reinstall / Clear Data: confirm favorites and history entries still show proper titles, authors and cover art from the cache.
- Primary-storage SAF books (Media/, Music/, Documents/) on Android 11+: open, play, seek, and confirm position saving works.
- RTR source: browse categories/listings, open book, search, pagination, playback.
- Playback controls under load: rapid pause/play/seek, track switching, Bluetooth/headset/media-button, Android Auto.
- Background playback, sleep timer, bookmarks (add/jump/delete), speed/pitch/skip-silence/normalize.
- Settings screens: toggle options rapidly and confirm no UI freezes.
- Verify localized strings are correct across all supported languages.

## Русский
# Примечания к выпуску — 0.0.55

Дата выпуска: 23-Apr-2026

## Русский
- История и Избранное теперь хранят встроенный кэш отображения: названия, авторы, исполнители, обложки и длительность остаются видимыми даже после переустановки приложения или «Очистки данных».
- Когда метаданные книги временно недоступны, в записях показывается читаемый запасной заголовок (например, ID видео YouTube или очищённое имя из пути), а не «сырой» идентификатор.
- Исправлена редкая проблема с появлением фантомной записи после некоторых переходов состояния.
- Исправлено воспроизведение из папок основного хранилища (Media/Music/Documents) на Android 11+: файлы, которые ранее падали с ошибкой доступа, теперь надёжно воспроизводятся через SAF-фолбэк, при этом сохранение позиции работает корректно.
- Исправлены редкие зависания интерфейса, вызванные синхронной записью настроек в главном потоке при высокой нагрузке; запись теперь неблокирующая.
- Расширена поддержка каталога провайдера RTR, включая больше категорий и вариантов сортировок.
- Более надёжное сохранение файла библиотеки stp.lib: устаревшие временные файлы больше не мешают записи истории/избранного, а ошибки записи сопровождаются более понятными сообщениями.
- Улучшена работа с веб-источниками: более устойчивые повторы и настроенные таймауты для RTR, что уменьшает временные сбои загрузки.
- Более согласованное объединение метаданных книг между обходами: лишние перезаписи исключены, меньше «мерцаний» деталей (исполнитель/жанр/описание) при втором проходе.
- В нерелизных сборках появилось журналирование в файл: ротация за 7 дней в папке внешних файлов приложения — помогает диагностировать проблемы.
- Обновлены переводы для всех поддерживаемых языков (DE, ES, FI, FR, JA, NL, PT, RU, SV, TR, ZH).

### Изменения поведения
- Списки Истории и Избранного теперь отображаются мгновенно из кэша stp.lib и обращаются к данным отдельной книги только при необходимости; хранилище книги остаётся источником истины для подробных данных.
- Синхронная запись настроек из главного потока автоматически заменяется на асинхронную, чтобы избежать подвисаний интерфейса.

### НЕСОВМЕСТИМЫЕ ИЗМЕНЕНИЯ
- Отсутствуют

### Риски / Что проверить
- Путь обновления: существующие данные истории/избранного из 0.0.54 должны загружаться и затем пересохраняться в новом формате.
- Откат на 0.0.54 не поддерживается — убедитесь, что это соответствует ожиданиям пользователей.
- Переустановка / Очистка данных: проверьте, что в Избранном и Истории сохраняются корректные заголовки, авторы и обложки из кэша.
- Книги в основном хранилище через SAF (Media/, Music/, Documents/) на Android 11+: открытие, воспроизведение, перемотка и сохранение позиции.
- Источник RTR: навигация по категориям/сортировкам, открытие книги, поиск, постраничная загрузка, воспроизведение.
- Управление воспроизведением под нагрузкой: быстрое pause/play/seek, переключение треков, Bluetooth/гарнитура/медиа-кнопки, Android Auto.
- Фоновое воспроизведение, таймер сна, закладки (добавление/переход/удаление), скорость/тональность/пропуск тишины/нормализация.
- Экраны настроек: быстрое переключение опций — убедиться, что нет зависаний интерфейса.
- Проверить корректность переведённых строк на всех поддерживаемых языках.
