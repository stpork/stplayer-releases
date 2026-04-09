# Release notes — 0.0.50

Release date: 09-Apr-2026

## English
- Fixed cases where tapping the playback notification or system mini-player reopened the wrong book. It now returns to the active book more reliably, including after restore.
- YouTube source search now keeps the selected section, time period, and media/playlists filter, and refreshes correctly when the query changes.
- Improved playback reliability for some web sources when stream links depend on the current source domain.
- The standard release build now uses a self-contained built-in source catalog, improving source availability after installs and updates.

### Behavior changes
- The standard release build now relies on the app’s built-in source catalog instead of custom external source packs.
- Opening the app from active playback should land on the current book more consistently.
- YouTube searches now stay tied to the current browsing context instead of falling back to a generic search state.

### BREAKING CHANGES
- Custom external source packs or manual source overrides are no longer applied in the standard release build.

### Risks / What to test
- Update from the previous version and confirm all expected sources appear and open normally.
- Start a book, open it from the notification or system mini-player, and confirm it returns to the same book.
- In the YouTube source, change section/sort/filter, run a search, then change the query again and confirm results refresh correctly.
- Re-check any workflow that depended on custom external source packs.

## Русский
- Исправлены случаи, когда нажатие на уведомление о воспроизведении или системный мини-плеер открывало не ту книгу. Теперь приложение надежнее возвращает к активной книге, в том числе после восстановления.
- Поиск в источнике YouTube теперь сохраняет выбранный раздел, период и фильтр «медиа/плейлисты», а также корректно обновляется при изменении запроса.
- Повышена надежность воспроизведения для некоторых веб-источников, где ссылки на поток зависят от текущего домена источника.
- Стандартная release-сборка теперь использует самодостаточный встроенный каталог источников, что улучшает доступность источников после установки и обновлений.

### Изменения в поведении
- Стандартная release-сборка теперь использует встроенный каталог источников вместо пользовательских внешних пакетов источников.
- При открытии приложения из активного воспроизведения оно должно стабильнее возвращать к текущей книге.
- Поиск в YouTube теперь остается привязанным к текущему контексту просмотра и не сбрасывается в общий режим поиска.

### Ломающие изменения
- Пользовательские внешние пакеты источников и ручные переопределения источников больше не применяются в стандартной release-сборке.

### Риски / Что проверить
- Обновитесь с предыдущей версии и проверьте, что все ожидаемые источники отображаются и открываются нормально.
- Запустите книгу, откройте ее из уведомления или системного мини-плеера и проверьте, что открывается та же книга.
- В источнике YouTube измените раздел/сортировку/фильтр, выполните поиск, затем измените запрос еще раз и проверьте, что результаты обновляются корректно.
- Повторно проверьте любые сценарии, которые зависели от пользовательских внешних пакетов источников.