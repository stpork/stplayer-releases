# Release notes — 0.0.56

Release date: 23-Apr-2026

## English
- History and Favorites now keep a built-in display cache, so titles, authors, performers, cover art and duration stay visible even after a reinstall or "Clear data".
- When book metadata is temporarily unavailable, entries show a human-readable fallback title (e.g. a YouTube video ID or a cleaned-up path name) instead of a raw identifier.
- Fixed playback on primary-storage folders (Media/Music/Documents) on Android 11+: files that previously failed with permission errors now play reliably, and position tracking is preserved.
- Fixed rare UI freezes caused by settings being written synchronously on the main thread under heavy write load; writes are now non-blocking.
- Changing a category from the pull-to-refresh/list control now takes effect immediately instead of being ignored.
- More reliable saving of the library file: stale temporary files no longer block history/favorites from being written, and write failures are logged with clearer reasons.
- Fixed a rare issue where a phantom entry could appear in lists after certain state transitions.
- Expanded catalog support for one of the online sources, including a wider set of categories and listings, with more resilient retries and tuned timeouts that reduce transient loading failures.
- More consistent merging of book metadata across scrapes, reducing flicker of performer, genre and description on second-pass refresh.
- Reduced background network load and memory pressure by removing an aggressive background detail fetch that could cause rate-limit storms and out-of-memory conditions.
- Artwork loading is more reliable on servers that mishandle compressed responses.
- New in-app file logging for non-release builds: a rolling 7-day log is saved to the app's external files folder to help diagnose issues.
- Translations refreshed across all supported languages (DE, ES, FI, FR, JA, NL, PT, RU, SV, TR, ZH).

### Behavior changes
- History and Favorites remain visually populated after a reinstall or "Clear data" (titles, covers, durations) even before any re-scrape.
- Unknown entries now display a readable fallback name instead of a raw identifier.
- Saving preferences no longer blocks the UI thread under heavy load.
- Category changes in the list apply immediately.

### BREAKING CHANGES
- None

### Risks / What to test
- Open History and Favorites after a reinstall or "Clear data": entries should show titles, authors, covers and durations from the cache.
- Play files stored in primary-storage Media/Music/Documents folders on Android 11+: playback should start and position should be saved.
- Change a category from the pull-to-refresh control: the new category should apply right away.
- Rapidly toggle settings (speed, skip silence, normalize, sleep timer) during playback: UI should remain responsive.
- Browse the online source catalogs, including the expanded set of categories and listings; transient loading errors should recover on retry.
- Validate History/Favorites persistence across app restarts and upgrades from 0.0.54/0.0.55.
- Verify artwork appears correctly for books where covers previously failed to load.

## Русский
# Примечания к релизу — 0.0.56

Дата релиза: 23-апр-2026

## Русский
- История и Избранное теперь хранят встроенный кэш отображения, поэтому названия, авторы, исполнители, обложки и длительность остаются видимыми даже после переустановки или «Очистки данных».
- Когда метаданные книги временно недоступны, записи показывают читаемое резервное название (например, идентификатор видео YouTube или очищенное имя пути) вместо сырого идентификатора.
- Исправлено воспроизведение из папок основного хранилища (Media/Music/Documents) на Android 11+: файлы, ранее падавшие с ошибкой доступа, теперь воспроизводятся надёжно, а позиция сохраняется.
- Устранены редкие зависания интерфейса, вызванные синхронной записью настроек в главном потоке при большой нагрузке; запись теперь неблокирующая.
- Смена категории через элемент управления «потяните для обновления»/список теперь применяется немедленно, а не игнорируется.
- Более надёжное сохранение файла библиотеки: устаревшие временные файлы больше не блокируют запись истории и избранного, а причины сбоев записываются с более понятными пояснениями.
- Исправлена редкая ошибка, при которой в списках мог появляться фантомный элемент после определённых переходов состояния.
- Расширена поддержка каталога одного из онлайн-источников, включая более широкий набор категорий и подборок, с более устойчивыми повторами запросов и настроенными таймаутами, снижающими временные сбои загрузки.
- Более согласованное объединение метаданных книг между запросами, снижающее мерцание исполнителя, жанра и описания при повторном обновлении.
- Снижена фоновая сетевая нагрузка и расход памяти за счёт отключения агрессивной фоновой загрузки деталей, которая могла вызывать шквал ограничений по частоте и нехватку памяти.
- Загрузка обложек стала надёжнее на серверах, некорректно обрабатывающих сжатые ответы.
- Новое внутреннее файловое логирование для нерелизных сборок: скользящий 7-дневный журнал сохраняется во внешнюю папку приложения для диагностики проблем.
- Обновлены переводы для всех поддерживаемых языков (DE, ES, FI, FR, JA, NL, PT, RU, SV, TR, ZH).

### Изменения поведения
- История и Избранное визуально остаются заполненными после переустановки или «Очистки данных» (названия, обложки, длительности) ещё до повторного сканирования.
- Неизвестные записи теперь отображают читаемое резервное имя вместо сырого идентификатора.
- Сохранение настроек больше не блокирует интерфейс под высокой нагрузкой.
- Смена категории в списке применяется сразу.

### BREAKING CHANGES
- Нет

### Риски / Что проверить
- Открыть Историю и Избранное после переустановки или «Очистки данных»: записи должны показывать названия, авторов, обложки и длительность из кэша.
- Воспроизвести файлы из папок основного хранилища Media/Music/Documents на Android 11+: воспроизведение должно запускаться, позиция — сохраняться.
- Сменить категорию через элемент управления обновлением: новая категория должна применяться сразу.
- Быстро переключать настройки (скорость, пропуск тишины, нормализация, таймер сна) во время воспроизведения: интерфейс должен оставаться отзывчивым.
- Просматривать каталоги онлайн-источников, включая расширенный набор категорий и подборок; временные ошибки загрузки должны восстанавливаться при повторе.
- Проверить сохранность Истории/Избранного между перезапусками приложения и при обновлении с 0.0.54/0.0.55.
- Убедиться, что обложки корректно отображаются для книг, у которых ранее они не загружались.
