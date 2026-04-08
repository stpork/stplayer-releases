# Release notes — 0.0.34

Release date: 15-Mar-2026

## English
- Playback now properly resumes paused books when you tap them from History or Library — previously, tapping a paused book would either skip it or restart from the beginning.
- Sleep timer is more reliable in the background — fixed cases where the timer would fail to stop playback after expiring, especially when the app wasn't visible.
- Battery usage reduced during torrent playback — the app no longer holds a wake lock while waiting for data to download in STATE_BUFFERING, which could drain 5-8 mAh per session.
- Download progress is now accurate for tracks without known file sizes — previously, unsized tracks could cause the overall progress to jump or stall incorrectly.
- Fixed book artwork and source details not appearing when reopening books from History or Favorites.
- Multi-track books now display correctly on Bluetooth headphones, car systems, and Android Auto (showing "N. BookTitle" format).
- Fixed stuck notifications and lingering playback controls that could appear after stopping playback.

### Behavior changes
- Large UI text size (UIScale.LARGE) now works as expected instead of being silently reduced to medium.
- Torrent downloads that fail before completion now properly clean up, preventing handles from lingering and causing future issues.

### BREAKING CHANGES
- None

### Risks / What to test
- Resume playback from History and Library after pausing a book.
- Sleep timer expiration while the app is in the background.
- Download progress accuracy for HLS/web downloads with multiple tracks.
- Bluetooth and Android Auto playback with multi-track audiobooks.

## Русский
- Воспроизведение теперь корректно возобновляет приостановленные книги при нажатии из Истории или Библиотеки — раньше при нажатии на приостановленную книгу она либо пропускалась, либо начиналась заново.
- Таймер сна стал более надёжным в фоновом режиме — исправлены случаи, когда таймер не останавливал воспроизведение после истечения, особенно когда приложение не было видно.
- Уменьшено энергопотребление при торрент-воспроизведении — приложение больше не удерживает wake lock в состоянии STATE_BUFFERING во время загрузки данных, что могло расходовать 5-8 мАч за сеанс.
- Прогресс загрузки теперь точен для треков без известного размера файла — ранее треки без размера могли вызывать скачки или остановку общего прогресса.
- Исправлено отсутствие обложек и информации об источнике при повторном открытии книг из Истории или Избранного.
- Многотрековые книги теперь корректно отображаются на Bluetooth-наушниках, автомобильных системах и Android Auto (формат "N. Название книги").
- Исправлены зависшие уведомления и остающиеся элементы управления воспроизведением, которые могли появляться после остановки.

### Изменения поведения
- Крупный размер текста интерфейса (UIScale.LARGE) теперь работает как положено вместо того, чтобы тихо уменьшаться до среднего.
- Незавершённые торрент-загрузки теперь корректно очищаются, предотвращая утечки данных и проблемы в будущем.

### Критические изменения
- Отсутствуют

### Что тестировать
- Возобновление воспроизведения из Истории и Библиотеки после приостановки книги.
- Срабатывание таймера сна в фоновом режиме.
- Точность прогресса загрузки для HLS/веб-загрузок с несколькими треками.
- Воспроизведение на Bluetooth и Android Auto с многотрековыми аудиокнигами.
