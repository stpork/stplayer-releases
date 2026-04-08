# Release notes — 0.0.20

Release date: 18-Feb-2026 

## English
- Improved playback reliability across local files, web sources, and torrents, especially during app/service lifecycle changes.
- Better resume behavior: playback now restores more consistently from your last valid position in history.
- More robust source parsing and pagination, so book lists and track links load more consistently from supported catalogs.
- Improved metadata and cover handling for library items, with more consistent durations and artwork resolution.
- Storage folder setup is now safer: invalid root-folder choices and overlapping library roots are blocked with clearer guidance.

### Behavior changes
- When choosing a storage folder, selecting the storage root itself is now rejected.
- Folder selections that overlap an already configured root are now rejected.
- Resume-from-history now falls back more reliably to the best available saved position.

### BREAKING CHANGES
- None

### Risks / What to test
- Re-select storage folders and verify invalid/overlapping paths are blocked with clear messages.
- Open several web-source catalogs and confirm listing pagination and track loading work as expected.
- Resume a few books from history (local/web/torrent) and verify position restoration accuracy.
- Check several library items for correct duration display and cover artwork.

## Русский
- Улучшена надежность воспроизведения для локальных файлов, веб-источников и торрентов, особенно при смене состояния приложения/сервиса.
- Улучшено возобновление: воспроизведение теперь стабильнее восстанавливается с последней корректной позиции из истории.
- Повышена устойчивость парсинга источников и пагинации, поэтому списки книг и ссылки на треки загружаются стабильнее в поддерживаемых каталогах.
- Улучшена работа с метаданными и обложками в библиотеке: длительности и обложки отображаются более последовательно.
- Настройка папок хранения стала безопаснее: недопустимый выбор корневой папки и пересекающиеся корни библиотеки блокируются с более понятными подсказками.

### Behavior changes
- При выборе папки хранения теперь нельзя выбрать сам корень хранилища.
- Выбор папки, пересекающейся с уже настроенным корнем, теперь отклоняется.
- Восстановление из истории теперь надежнее использует лучшую доступную сохраненную позицию.

### BREAKING CHANGES
- None

### Risks / What to test
- Повторно выбрать папки хранения и проверить, что недопустимые/пересекающиеся пути блокируются с понятными сообщениями.
- Открыть несколько веб-источников и проверить корректность пагинации и загрузки треков.
- Возобновить несколько книг из истории (локально/веб/торрент) и проверить точность восстановления позиции.
- Проверить несколько элементов библиотеки на корректное отображение длительности и обложек.