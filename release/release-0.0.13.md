# Release notes — 0.0.12.1

Release date: 12-Feb-2026 

## English
- The app now restores your last Library context after restart, including tab, mode (normal/search/category), selected source/list, and scroll position.
- Resume playback is more accurate for multi-track books by matching the saved track directly and resolving position more reliably when playlist data changes.
- Fixed cases where resume could jump to the wrong track near track boundaries; playback now resumes closer to the exact saved point.
- Improved progress/history loading for local and SAF sources, including better handling of folder vs file URIs.
- Listening progress in Library cards is now more stable for multi-track content and refreshes after position saves.
- Position saving is more reliable during pause, book switch, audio focus loss, and app stop, reducing chances of lost or stale progress.

### Behavior changes
- Library screen state is persisted and restored between app launches.
- Multi-track resume prioritizes saved track identity over stale index values.
- Live progress display is limited to safe cases (single-track playback), while persisted progress is used for multi-track items.
- Position updates from audio-focus and stop events are handled more deterministically.

### BREAKING CHANGES
- None

### Risks / What to test
- Restart the app from different Library contexts and confirm exact restore (tab, filters/search, scroll).
- Resume several multi-track books with changed track order and verify correct track/position.
- Test SAF and local-folder books opened from both folder and track entry points.
- Trigger audio focus loss (call/notification) and confirm progress is saved and resumed correctly.
- Switch books quickly and verify last position is not overwritten by older saves.

## Русский
- Теперь приложение восстанавливает последний контекст Библиотеки после перезапуска: вкладку, режим (обычный/поиск/категория), выбранный источник/список и позицию прокрутки.
- Возобновление воспроизведения стало точнее для многотрековых книг: сохраненный трек сопоставляется напрямую, а позиция восстанавливается надежнее даже при изменении плейлиста.
- Исправлены случаи, когда возобновление могло перейти на неверный трек рядом с границами треков; теперь воспроизведение продолжается ближе к точной сохраненной точке.
- Улучшена загрузка прогресса и истории для локальных и SAF-источников, включая более корректную обработку URI папок и файлов.
- Прогресс прослушивания в карточках Библиотеки стал стабильнее для многотрекового контента и обновляется после сохранения позиции.
- Сохранение позиции стало надежнее при паузе, переключении книги, потере аудиофокуса и остановке приложения, что снижает риск потери или перезаписи прогресса.

### Изменения поведения
- Состояние экрана Библиотеки сохраняется и восстанавливается между запусками приложения.
- Для многотрекового возобновления приоритет отдается идентичности сохраненного трека, а не устаревшему индексу.
- Онлайн-обновление прогресса применяется только в безопасных случаях (один трек), а для многотрековых элементов используется сохраненный прогресс.
- Обновления позиции при событиях аудиофокуса и остановки обрабатываются более детерминированно.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
- None

### Риски / Что протестировать
- Перезапуск приложения из разных состояний Библиотеки и проверка точного восстановления (вкладка, фильтры/поиск, прокрутка).
- Возобновление нескольких многотрековых книг при измененном порядке треков: правильный трек и позиция.
- Проверка книг SAF и локальных папок при открытии как из папки, так и из точки входа трека.
- Имитация потери аудиофокуса (звонок/уведомление) и проверка корректного сохранения/восстановления прогресса.
- Быстрое переключение между книгами и проверка, что последняя позиция не перезаписывается более старым сохранением.