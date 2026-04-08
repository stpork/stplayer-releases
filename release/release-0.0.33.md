# Release notes — 0.0.33

Release date: 11-Mar-2026 

## English
- Reduced cases where playback leaves behind stuck notifications or lingering system playback controls.
- Sleep timer expiration is more reliable, especially when the app is in the background.
- Swipe navigation from Library, History, and Favorites now tracks the correct book more consistently, even after scrolling.
- Reopening books from History and Favorites now restores source details and artwork more reliably.
- Source tabs are less likely to open blank or stale on app start or when switching between sources.
- The library is better at marking the currently playing book and clearing temporary playback-start indicators once playback begins.
- Web and HLS downloads now show more accurate progress, and split tracks keep better names and durations after download.
- Torrent downloads now catch oversized torrents, low storage, and incomplete copied files earlier, with clearer error messages.

### Behavior changes
- Dismissing the playback notification now ends the current playback session cleanly.
- Long-paused, stalled, or errored playback sessions may now close themselves automatically instead of lingering in system controls.
- Horizontal swipe previews in Library, History, and Favorites now follow the book under your finger more closely.

### BREAKING CHANGES
- None

### Risks / What to test
- Dismiss the playback notification while playing and while paused, and confirm the session closes cleanly.
- Let the sleep timer expire in both foreground and background, and confirm playback pauses as expected.
- Swipe from Library, History, and Favorites into book or player views after scrolling, and confirm the correct item opens.
- Switch sources on startup and during normal use, and confirm the first page loads without blank or stale content.
- Download a web/HLS book and a torrent book, and verify progress, track names, durations, and clear low-storage or copy-failure errors.

## Русский
- Стало меньше случаев, когда после воспроизведения остаются зависшие уведомления или системные элементы управления.
- Срабатывание таймера сна стало надежнее, особенно когда приложение работает в фоне.
- Свайпы из Библиотеки, Истории и Избранного теперь стабильнее выбирают нужную книгу даже после прокрутки.
- При повторном открытии книг из Истории и Избранного теперь надежнее восстанавливаются источник, детали книги и обложка.
- Вкладки источников реже открываются пустыми или с устаревшим содержимым при запуске приложения и переключении между источниками.
- Библиотека точнее определяет текущую воспроизводимую книгу и быстрее убирает временный индикатор запуска воспроизведения.
- Для веб- и HLS-загрузок прогресс стал точнее, а у разбитых на части дорожек лучше сохраняются названия и длительность после загрузки.
- Torrent-загрузки теперь раньше останавливаются при слишком большом размере, нехватке места или неполном копировании файлов и показывают более понятные ошибки.

### Изменения в поведении
- Закрытие уведомления воспроизведения теперь корректно завершает текущую сессию.
- Сеансы с длительной паузой, зависанием или ошибкой теперь могут завершаться автоматически, а не оставаться в системных элементах управления.
- Горизонтальные свайп-превью в Библиотеке, Истории и Избранном теперь точнее следуют за книгой под пальцем.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
- Нет

### Риски / Что проверить
- Закройте уведомление воспроизведения во время проигрывания и на паузе и убедитесь, что сессия завершается корректно.
- Дайте таймеру сна сработать и на переднем плане, и в фоне, и проверьте, что воспроизведение останавливается как ожидается.
- Сделайте свайп из Библиотеки, Истории и Избранного в экран книги или проигрывателя после прокрутки и проверьте, что открывается правильный элемент.
- Переключайте источники при запуске приложения и в обычной работе и убедитесь, что первая страница загружается без пустого или устаревшего содержимого.
- Скачайте одну веб/HLS-книгу и одну torrent-книгу и проверьте прогресс, названия дорожек, длительность и понятные ошибки при нехватке места или сбое копирования.