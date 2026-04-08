# Release notes — 0.0.45

Release date: 02-Apr-2026

## English
- Android Auto now uses a single `Sources` entry that follows the same order and visibility as your main library tabs.
- Android Auto source pages now show filters like categories and sort options before the book list, so deep browsing is faster.
- Cover art now appears more reliably for local folders, downloads, and other private files across the Library, History, notifications, and Android Auto.
- Background playback controls are more reliable: repeated headset and media-button signals are less likely to trigger double starts, and notification actions wake the player more consistently from the background.
- Library startup and source navigation are more consistent: the app restores your last opened view more reliably, and sources open on their intended default feed or sort more often.
- Saved books now reconnect to their original source more reliably in History and Favorites, improving reopen behavior and artwork loading.
- Favoriting web books, local folders, and books opened through the system file picker works better even before they have a full History entry.
- Downloaded books are recognized more reliably after refresh or restart, including relinked folders and partial downloads, so download badges and actions stay in sync.
- Aknigi24 books now open more reliably when the site serves direct chapter files instead of the older ZIP package.
- Protected links now fail cleanly on a wrong password instead of sometimes showing corrupted text.

### Behavior changes
- On first launch, STPlayer still prefers the first visible online source, while returning users should land back on their last opened library view more consistently.
- If a book load is canceled because you switch to something else, the old request is less likely to continue and start the wrong book.
- If a book is favorited before it exists in History, STPlayer now creates the saved entry it needs automatically.
- Relinking an existing downloaded folder now restores its downloaded state immediately in the library.

### BREAKING CHANGES
None

### Risks / What to test
- Check Android Auto: open `Sources`, enter a source, and confirm categories and sort options appear before the book list.
- Verify cover art for local folders, books opened through the system file picker, downloads, notifications, and Android Auto.
- Test headset, Bluetooth, media buttons, and notification controls from the background and confirm playback does not start twice.
- Add a web book, a local folder, and a system file picker book to Favorites before fully playing them, then reopen them from Favorites and History.
- Restart the app and confirm downloaded books, relinked downloads, and partial downloads keep the correct badges and actions.
- Test Aknigi24 books that expose direct `part` files and confirm playback starts normally.
- Enter a wrong password for protected content and confirm the app fails cleanly without corrupted text.

## Русский
- В Android Auto теперь используется единый раздел `Sources`, который повторяет порядок и видимость вкладок основной библиотеки.
- На страницах источников в Android Auto фильтры, категории и сортировки теперь показываются перед списком книг, поэтому по большим каталогам стало быстрее перемещаться.
- Обложки теперь надежнее показываются для локальных папок, загрузок и других приватных файлов в Библиотеке, Истории, уведомлениях и Android Auto.
- Фоновые элементы управления воспроизведением стали надежнее: повторные сигналы с гарнитуры и медиакнопок реже вызывают двойной запуск, а действия из уведомления стабильнее будят плеер из фона.
- Запуск библиотеки и переходы по источникам стали стабильнее: приложение надежнее восстанавливает последнюю открытую вкладку, а источники чаще открываются сразу на нужной ленте или сортировке.
- Сохраненные книги теперь надежнее привязываются к исходному источнику в Истории и Избранном, что улучшает повторное открытие и загрузку обложек.
- Добавление веб-книг, локальных папок и книг, открытых через системный выбор файлов, в Избранное теперь работает лучше даже до появления полной записи в Истории.
- Загруженные книги теперь надежнее распознаются после обновления или перезапуска, включая перепривязанные папки и частичные загрузки, поэтому значки и действия загрузки остаются синхронизированными.
- Книги с Aknigi24 теперь надежнее открываются, когда сайт отдает прямые файлы глав вместо старого ZIP-пакета.
- Защищенные ссылки теперь корректно завершаются ошибкой при неверном пароле вместо появления поврежденного текста.

### Изменения в поведении
- При первом запуске STPlayer по-прежнему предпочитает первый видимый онлайн-источник, а для возвращающихся пользователей надежнее восстанавливает последнюю открытую вкладку библиотеки.
- Если загрузка книги отменяется из-за переключения на другую книгу, старый запрос теперь реже продолжает работу и запускает не ту книгу.
- Если книгу добавляют в Избранное до появления записи в Истории, STPlayer теперь автоматически создает нужную сохраненную запись.
- Повторная привязка уже существующей папки загрузки теперь сразу возвращает ей статус загруженной в библиотеке.

### Ломающие изменения
Нет

### Риски / Что проверить
- Проверьте Android Auto: откройте `Sources`, зайдите в источник и убедитесь, что категории и сортировки идут перед списком книг.
- Проверьте обложки для локальных папок, книг из системного выбора файлов, загрузок, уведомлений и Android Auto.
- Проверьте гарнитуру, Bluetooth, медиакнопки и действия из уведомления из фона: воспроизведение не должно запускаться дважды.
- Добавьте веб-книгу, локальную папку и книгу из системного выбора файлов в Избранное до полного воспроизведения, затем откройте их из Избранного и Истории.
- Перезапустите приложение и убедитесь, что загруженные книги, перепривязанные загрузки и частичные загрузки сохраняют правильные значки и действия.
- Проверьте книги с Aknigi24, где доступны прямые `part`-файлы, и убедитесь, что воспроизведение запускается нормально.
- Введите неверный пароль для защищенного контента и убедитесь, что приложение показывает корректную ошибку без поврежденного текста.