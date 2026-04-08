# Release notes — 0.0.42

Release date: 31-Mar-2026 

## English
- History, Favorites, downloads, and resume are better at recognizing the same book even if it was previously stored under a different internal ID. This reduces duplicate entries and cases where the app reopens the wrong book.
- Adding to Favorites now works more reliably for books opened directly from folders, web streams, or torrents, even before they have a stable History entry.
- Downloaded books are found and reopened more reliably when you return to them later, even if older saved link data is stale.
- Restoring your last session after an app or service restart is more accurate, with better recovery of the right playlist, track, speed, and saved position.
- If folder access is no longer available, the app now avoids trying to auto-resume a broken item.
- Notification and system player taps open the Player screen more reliably for the current book.
- When the bottom player bar is collapsed, opening the full Player temporarily expands the controls so playback actions are immediately available.

### Behavior changes
- Some older duplicate History cards may merge after updating if they point to the same book.
- Notification and system player taps now open Player directly on the current book.
- The full Player temporarily expands collapsed bottom controls.
- Auto-restore now skips folder-based books that no longer have storage access.

### BREAKING CHANGES
- None

### Risks / What to test
- Update from `0.0.41` and confirm History and Favorites still open the correct books.
- Add a new folder/web/torrent book to Favorites before it appears in History.
- Reopen an older downloaded book and confirm offline playback starts and resumes correctly.
- Restart the app, then resume from the notification or system player and verify the correct book, track, speed, and position.
- Revoke access to a previously selected folder and confirm the app fails safely instead of trying to auto-resume it.

## Русский
- История, Избранное, загрузки и восстановление воспроизведения теперь лучше распознают одну и ту же книгу, даже если раньше она была сохранена под другим внутренним ID. Это уменьшает количество дубликатов и снижает случаи, когда приложение повторно открывает не ту книгу.
- Добавление в Избранное теперь надёжнее работает для книг, открытых прямо из папок, web-потоков или torrent-источников, даже если у них ещё нет устойчивой записи в Истории.
- Загруженные книги теперь чаще находятся и корректно открываются при повторном возврате к ним, даже если старые сохранённые данные о ссылке устарели.
- Восстановление последней сессии после перезапуска приложения или фонового сервиса стало точнее: лучше восстанавливаются нужные плейлист, трек, скорость и сохранённая позиция.
- Если доступ к папке больше недоступен, приложение теперь не пытается автоматически восстановить заведомо сломанный элемент.
- Нажатия из уведомления и системного плеера теперь надёжнее открывают экран Player для текущей книги.
- Если нижняя панель плеера свернута, при открытии полного экрана Player элементы управления временно разворачиваются, поэтому основные действия доступны сразу.

### Изменения в поведении
- Некоторые старые дубликаты карточек в Истории после обновления могут объединиться в одну запись, если они относятся к одной и той же книге.
- Нажатия из уведомления и системного плеера теперь открывают Player сразу на текущей книге.
- На полном экране Player временно разворачиваются свернутые нижние элементы управления.
- Автовосстановление теперь пропускает книги из папок, если доступ к хранилищу уже потерян.

### Ломающие изменения
- Нет

### Риски / Что проверить
- Обновиться с `0.0.41` и проверить, что История и Избранное по-прежнему открывают правильные книги.
- Добавить новую книгу из папки, web-источника или torrent-источника в Избранное до того, как она появится в Истории.
- Повторно открыть ранее загруженную книгу и убедиться, что офлайн-воспроизведение запускается и продолжаетcя корректно.
- Перезапустить приложение, затем возобновить воспроизведение из уведомления или системного плеера и проверить правильные книгу, трек, скорость и позицию.
- Отозвать доступ к ранее выбранной папке и убедиться, что приложение безопасно обрабатывает ситуацию и не пытается автоматически восстановить недоступный элемент.