# Release notes — 0.0.8

Release date: 10-Feb-2026 

## English
- Improved download folder selection: the system picker now opens with proper access flags, and folder re-selection is smoother from Settings.
- Storage permission handling is clearer: browsing/playing local folders works with read access, while downloads correctly require write access.
- Fixed stability issues during download checks and start flow; failed download decisions now show a clear error instead of causing crashes.
- Listening progress in the library now refreshes more reliably for currently playing books, including persisted progress updates.
- Fixed progress/history matching for local and SAF folder sources, improving resume accuracy after folder-based playback.
- Improved remote source browsing: category URLs are resolved more reliably (including relative links), reducing failed category loads.
- Added clearer pagination failure feedback and pull-to-refresh haptic confirmation when refresh is ready.

### Behavior changes
- Downloads now require confirmed read + write permission for the selected download folder.
- Read-only SAF access remains valid for browsing and playback workflows.
- Pull-to-refresh gives haptic confirmation when the gesture reaches the refresh trigger threshold.
- When loading additional pages fails, the app now shows a visible error toast with request context.

### BREAKING CHANGES
- None

### Risks / What to test
- Verify download start/end flow from both Library and Book screens, including overwrite flows.
- Verify folder picker behavior when current folder is valid, missing, read-only, or revoked.
- Verify library progress bar updates while a book is actively playing.
- Verify category browsing and pagination on sources that use relative URLs.
- Verify pull-to-refresh feedback and refresh triggering on supported devices.

## Русский
- Улучшен выбор папки для загрузок: системный выбор папки теперь запускается с корректными правами, а повторный выбор папки в настройках стал удобнее.
- Логика прав доступа к хранилищу стала понятнее: просмотр и воспроизведение локальных папок работают с правом чтения, а для загрузок корректно требуется право записи.
- Исправлены проблемы стабильности при проверке и запуске загрузок; при сбое теперь показывается понятная ошибка вместо падения приложения.
- Прогресс прослушивания в библиотеке теперь обновляется надежнее для текущей воспроизводимой книги, включая сохраненный прогресс.
- Исправлено сопоставление истории/прогресса для локальных и SAF-источников, что улучшает точность возобновления воспроизведения.
- Улучшена работа с удаленными источниками: URL категорий теперь корректнее обрабатываются (включая относительные ссылки), что снижает число ошибок загрузки категорий.
- Добавлена более понятная обратная связь при ошибках пагинации и тактильное подтверждение готовности pull-to-refresh.

### Изменения поведения
- Для загрузок теперь обязательно подтвержденное право чтения и записи в выбранной папке загрузки.
- Доступ SAF только на чтение остается достаточным для просмотра и воспроизведения.
- В pull-to-refresh добавлено тактильное подтверждение при достижении порога срабатывания обновления.
- При ошибке загрузки следующих страниц теперь показывается видимый toast с контекстом запроса.

### BREAKING CHANGES
- None

### Риски / Что протестировать
- Проверить полный сценарий загрузки (старт/завершение) на экранах Library и Book, включая сценарии перезаписи.
- Проверить поведение выбора папки, когда текущая папка валидна, недоступна, только для чтения или с отозванными правами.
- Проверить обновление индикатора прогресса в библиотеке во время активного воспроизведения.
- Проверить открытие категорий и пагинацию на источниках с относительными URL.
- Проверить тактильную обратную связь и запуск обновления через pull-to-refresh на поддерживаемых устройствах.