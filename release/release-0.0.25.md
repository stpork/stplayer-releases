# Release notes — 0.0.25

Release date: 24-Feb-2026 

## English
- Added a TV-optimized experience with Android TV launcher support, TV home browsing, details view, and player controls built for remote navigation.
- Added Android Auto media browsing support, including Continue, Recent, Favorites, Sources, and in-car search/playback flows.
- Added a new setting for mini-player artwork progress: show progress on artwork always, or only while seeking.
- Improved mini-player progress feedback with a persistent percentage option when enabled.
- Improved tap/scroll gesture handling to reduce accidental playback starts after scrolling.
- Fixed swipe-to-delete targeting in History and Favorites so gestures more reliably affect the intended card.
- Fixed duplicate-entry handling in History/Favorites so remove actions are applied to the correct source/folder item.
- Fixed cases where deleted history items could reappear unexpectedly after background updates.
- Improved resume behavior: when no valid saved position is found, playback now starts from the beginning instead of failing.
- Improved Favorites metadata/artwork loading and large-list sorting responsiveness.
- Improved localization and UI text consistency across supported languages, including clearer empty/error and folder-access messages.

### Behavior changes
- On TV devices, the app now opens a TV-specific UI automatically.
- In mini-player settings, artwork progress display can now be switched between `Always` and `Seek only`.
- Removing an item from History/Favorites now targets that specific source/folder entry instead of broadly matching by title/ID alone.
- If resume data is unavailable, playback now starts at the beginning.

### BREAKING CHANGES
- None

### Risks / What to test
- TV navigation and playback flow (Home → Details → Player) with a remote.
- Android Auto browse/search/playback from each root section.
- Mini-player progress display behavior in both setting modes.
- Swipe-delete and context-menu delete in History/Favorites with duplicate titles from different sources.
- Resume behavior for items with missing/invalid saved position.

## Русский
- Добавлен интерфейс для ТВ с поддержкой запуска на Android TV, просмотром домашнего экрана, карточкой книги и плеером для управления с пульта.
- Добавлена поддержка Android Auto: разделы Продолжить, Недавние, Избранное, Источники, а также поиск и запуск в автомобиле.
- Добавлена новая настройка прогресса на обложке мини-плеера: показывать всегда или только при перемотке.
- Улучшена индикация прогресса в мини-плеере: при включении доступен постоянный процент.
- Улучшена обработка касаний и скролла, чтобы снизить количество случайных запусков после прокрутки.
- Исправлено определение карточки при свайпе на удаление в Истории и Избранном.
- Исправлена работа с дубликатами в Истории/Избранном: удаление теперь применяется к правильному элементу источника/папки.
- Исправлены случаи, когда удалённые элементы истории могли неожиданно появляться снова после фоновых обновлений.
- Улучшено возобновление: если корректная сохранённая позиция не найдена, воспроизведение начинается с начала, а не завершается ошибкой.
- Улучшена загрузка метаданных/обложек в Избранном и отзывчивость сортировки в больших списках.
- Улучшены локализация и согласованность текстов интерфейса во всех поддерживаемых языках, включая более понятные пустые/ошибочные состояния и подсказки доступа к папкам.

### Behavior changes
- На ТВ-устройствах приложение теперь автоматически открывает специальный ТВ-интерфейс.
- В настройках мини-плеера теперь можно переключать отображение прогресса на обложке между `Always` и `Seek only`.
- Удаление из Истории/Избранного теперь применяется к конкретному элементу источника/папки, а не к широкому совпадению только по названию/ID.
- Если данные для возобновления недоступны, воспроизведение теперь начинается с начала.

### BREAKING CHANGES
- None

### Risks / What to test
- Навигация и воспроизведение на ТВ (Home → Details → Player) с пульта.
- Просмотр/поиск/воспроизведение в Android Auto из каждого корневого раздела.
- Поведение прогресса в мини-плеере в обоих режимах настройки.
- Удаление свайпом и через контекстное меню в Истории/Избранном при дубликатах из разных источников.
- Возобновление для элементов с отсутствующей/некорректной сохранённой позицией.