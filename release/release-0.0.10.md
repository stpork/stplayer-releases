# Release notes — 0.0.10

Release date: 11-Feb-2026 

## English
- Added full sorting for local SAF libraries: `Date`, `Name`, `Author`, and `Performer`.
- Improved local library browsing so category and sort selections are handled more reliably, including combined category+sort states.
- Fixed search behavior: “not found” results now show a normal empty state instead of a network/error state.
- Improved local permission recovery: previously selected folders are now restored more reliably when Android returns equivalent SAF URIs in a different format.
- Playback safety fix: if the saved queue no longer matches the saved track, autoplay is stopped to prevent playing the wrong item.
- Added clearer storage access error messages for invalid folder choices and overlapping media roots.

### Behavior changes
- Selecting the entire storage root is now blocked; you must choose a folder inside storage.
- Choosing a folder that overlaps another configured media root is now blocked.
- Re-selecting the same category or sort in the library no longer triggers unnecessary reload behavior.
- SAF “Date” sorting now follows real folder/file modification time more accurately.

### BREAKING CHANGES
- Users who previously selected a storage root directly may need to reselect a valid subfolder.

### Risks / What to test
- Verify SAF library sorting for all four sort modes.
- Verify folder selection rejects storage root and overlapping roots with correct messages.
- Verify search with no matches shows empty state (not error).
- Verify resume/autoplay behavior after modifying playlist order.

## Русский
- Добавлена полноценная сортировка для локальных SAF-библиотек: `Date`, `Name`, `Author`, `Performer`.
- Улучшена навигация по локальной библиотеке: выбор категории и сортировки теперь обрабатывается стабильнее, включая комбинированные состояния категория+сортировка.
- Исправлено поведение поиска: при отсутствии результатов теперь показывается обычное пустое состояние, а не состояние сетевой/транспортной ошибки.
- Улучшено восстановление локальных разрешений: ранее выбранные папки теперь надёжнее восстанавливаются, если Android возвращает эквивалентные SAF URI в другом формате.
- Исправление безопасности воспроизведения: если сохранённая очередь больше не совпадает с сохранённым треком, автозапуск отключается, чтобы не проигрывался неверный элемент.
- Добавлены более понятные сообщения об ошибках доступа к хранилищу для неверного выбора папки и пересекающихся корневых директорий.

### Behavior changes
- Выбор корня всего хранилища теперь запрещён; нужно выбирать папку внутри хранилища.
- Выбор папки, пересекающейся с уже настроенным корнем медиатеки, теперь запрещён.
- Повторный выбор той же категории или сортировки в библиотеке больше не запускает лишнюю перезагрузку.
- Сортировка SAF по `Date` теперь точнее использует реальное время изменения папок/файлов.

### BREAKING CHANGES
- Пользователям, которые ранее выбирали корень хранилища напрямую, может потребоваться повторно выбрать корректную вложенную папку.

### Risks / What to test
- Проверить сортировку SAF-библиотеки во всех четырёх режимах.
- Проверить, что выбор папки корректно отклоняет корень хранилища и пересекающиеся корни, с правильными сообщениями.
- Проверить, что поиск без совпадений показывает пустое состояние (а не ошибку).
- Проверить поведение восстановления/автозапуска после изменения порядка плейлиста.