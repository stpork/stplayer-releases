# Release notes — 0.0.30

Release date: 05-Mar-2026 

## English
- Improved playback resume accuracy across Library, History, Favorites, and external controls by using a unified start/resume flow.
- Fixed cases where playback from History could ignore saved progress (or start at `0:00`) under certain resume-mode settings.
- Improved position persistence reliability on app/service shutdown, reducing lost progress after background/lifecycle stops.
- History now deduplicates equivalent web-book entries more reliably, reducing repeated cards for the same book.
- Improved History loading indicators to prevent stale spinner states on cards after buffering state changes.
- Mini Player and playback metadata now avoid showing raw URLs as book titles when better metadata is available.
- Mini Player now shows a short position/progress hint when playback starts (when persistent artwork progress is disabled).
- Library search UX improvements: shorter minimum query length (2 chars), clearer pending-search state, better suggestion behavior, and one-tap clear-history.
- Search behavior is more predictable: remote search triggers on explicit submit, while typed text remains available for local filtering.
- Improved BYT source compatibility by refreshing client/session profiles, which helps browsing and playback reliability.

### Behavior changes
- Remote source search is now submit-driven (search button/IME), not auto-triggered while typing.
- Search history can now be cleared directly from the search suggestions menu.
- The app may show better canonical titles (instead of URL-like text) in Mini Player and external media surfaces.

### BREAKING CHANGES
- None

### Risks / What to test
- Resume from History/Favorites for local, SAF, web, and torrent books.
- App kill/service restart: confirm last position is restored correctly.
- Library search flow (typing vs submitted search) on sources with and without remote search.
- BYT browsing, search, and playback start on current endpoints.
- Android Auto/Bluetooth/lock-screen metadata title correctness.

## Русский
- Улучшена точность возобновления воспроизведения в Библиотеке, Истории, Избранном и при внешнем управлении благодаря единому сценарию старта/резюма.
- Исправлены случаи, когда запуск из Истории мог игнорировать сохранённый прогресс (или стартовать с `0:00`) при некоторых настройках режима возобновления.
- Повышена надёжность сохранения позиции при остановке приложения/сервиса, что снижает риск потери прогресса при фоновых и жизненных событиях.
- История теперь надёжнее объединяет одинаковые web-книги, уменьшая дубли карточек одной и той же книги.
- Улучшены индикаторы загрузки в Истории: устранены зависающие спиннеры на карточках после смены состояния буферизации.
- В мини-плеере и метаданных воспроизведения больше не показываются «сырые» URL как название книги, если доступны более корректные данные.
- В мини-плеере теперь кратко показывается подсказка по позиции/прогрессу при старте воспроизведения (если постоянный прогресс на обложке отключён).
- Улучшен UX поиска в Библиотеке: уменьшена минимальная длина запроса (до 2 символов), добавлен более понятный статус «поиск не отправлен», улучшены подсказки и добавлена очистка истории в один тап.
- Поведение поиска стало предсказуемее: удалённый поиск запускается только по явному подтверждению, а введённый текст продолжает использоваться для локальной фильтрации.
- Улучшена совместимость источника BYT за счёт обновления клиентских/сессионных профилей, что повышает стабильность просмотра и старта воспроизведения.

### Behavior changes
- Поиск по удалённым источникам теперь запускается по подтверждению (кнопка поиска/IME), а не автоматически при наборе.
- Историю поиска теперь можно очистить прямо из меню подсказок.
- Приложение может показывать более корректные названия (вместо URL-подобного текста) в мини-плеере и на внешних медиа-поверхностях.

### BREAKING CHANGES
- None

### Risks / What to test
- Возобновление из Истории/Избранного для локальных, SAF, web- и torrent-книг.
- Перезапуск после выгрузки приложения/сервиса: корректно ли восстанавливается последняя позиция.
- Сценарии поиска в Библиотеке (набор текста vs подтверждённый поиск) для источников с удалённым поиском и без него.
- Просмотр, поиск и старт воспроизведения в BYT на актуальных эндпоинтах.
- Корректность названий в метаданных для Android Auto/Bluetooth/экрана блокировки.