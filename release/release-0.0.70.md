I have enough context. Here are the release notes:

---

# Release notes — 0.0.70

Release date: 04-Jul-2026

## English

- **Full-text search now works correctly** on two major audiobook sources that previously returned empty or broken results when using the search bar.
- **Author and performer browsing fixed** on one source: tapping an author or performer category now opens the correct book list instead of returning a 404 error.
- **Default playback speed is now applied to new books.** When you set a preferred speed in Settings, it is used immediately when opening a book for the first time — not just for books you've played before.
- **Playback position no longer jumps back when pausing.** The progress bar now stays exactly where you stopped instead of snapping briefly to an earlier position.
- **After auto-advancing to the next track, the player no longer gets stuck on the loading spinner.** Playback continues smoothly across track boundaries.
- **Notification cover art is now shown correctly after a cold start.** The lock-screen/notification media widget now displays the correct book cover when the app is restored after being closed.
- **Restored position is more accurate after a force-close or crash.** The app now uses the most reliable position record available, reducing the chance of rewinding to an earlier point than where you stopped.
- **Media widget appears on the lock screen immediately after launch.** Previously, the notification-shade media controls were absent until the user explicitly pressed Play after a cold start.
- **Resuming playback from a cold-start restore (Bluetooth, headset button, notification) now works correctly.** Transport controls and external triggers would previously fail to start playback if the app was restored in a paused state.

### Behavior changes

- When opening a book for the first time, the player now inherits your configured default speed setting instead of always starting at 1.0×.

### BREAKING CHANGES

None

### Risks / What to test

- Search: verify results appear and are tappable on sources that support full-text search.
- Author/performer drill-down: browse by author or performer and confirm the book list loads.
- Cold-start restore: force-close the app mid-book, reopen, confirm position, cover art in notification, and that Bluetooth/headset resume works.
- Auto-advance: let a track finish naturally and confirm the spinner clears and the next track plays.
- Pause: confirm the progress bar does not jump backwards when pausing.
- New book, custom default speed: set a non-1× default speed, open a book never played before, confirm speed is applied.

---

## Русский

# Release notes — 0.0.70

Дата выпуска: 04-Jul-2026

- **Полнотекстовый поиск теперь работает корректно** на двух крупных источниках аудиокниг, где раньше строка поиска возвращала пустые или сломанные результаты.
- **Исправлен переход по авторам и исполнителям** на одном из источников: нажатие на автора или исполнителя теперь открывает правильный список книг вместо ошибки 404.
- **Скорость воспроизведения по умолчанию теперь применяется к новым книгам.** Если в настройках задана предпочтительная скорость, она будет использована сразу при открытии книги впервые — а не только для ранее прослушанных.
- **Позиция воспроизведения больше не прыгает назад при паузе.** Полоса прогресса теперь остаётся именно там, где вы остановились, без кратковременного отскока на более раннюю позицию.
- **После автоматического перехода к следующей дорожке плеер больше не зависает на индикаторе загрузки.** Воспроизведение теперь плавно продолжается при смене треков.
- **Обложка книги в уведомлении теперь отображается корректно после холодного запуска.** Медиа-виджет на экране блокировки и в шторке уведомлений теперь показывает правильную обложку при восстановлении приложения после закрытия.
- **Восстановленная позиция стала точнее после принудительного закрытия или краша.** Приложение теперь использует наиболее достоверную запись позиции, уменьшая вероятность «перемотки» к более ранней точке.
- **Медиа-виджет на экране блокировки появляется сразу после запуска.** Раньше элементы управления в шторке уведомлений отсутствовали до тех пор, пока пользователь явно не нажимал «Play» после холодного старта.
- **Возобновление воспроизведения после холодного старта (Bluetooth, кнопка наушников, уведомление) теперь работает корректно.** Ранее транспортные команды и внешние триггеры не запускали воспроизведение, если приложение было восстановлено в состоянии паузы.

### Изменения поведения

- При открытии книги впервые плеер теперь использует настроенную скорость по умолчанию вместо того, чтобы всегда начинать с 1.0×.

### Критические изменения

Нет

### Риски / Что тестировать

- Поиск: проверить, что результаты появляются и по ним можно переходить на источниках с полнотекстовым поиском.
- Переход по автору/исполнителю: открыть категорию автора или исполнителя и убедиться, что список книг загружается.
- Восстановление после холодного старта: принудительно закрыть приложение на середине книги, открыть снова, проверить позицию, обложку в уведомлении и то, что возобновление через Bluetooth/наушники работает.
- Автопереход треков: дать треку завершиться и убедиться, что индикатор загрузки пропадает и следующий трек воспроизводится.
- Пауза: убедиться, что полоса прогресса не прыгает назад при нажатии паузы.
- Новая книга, нестандартная скорость по умолчанию: задать скорость, отличную от 1×, открыть книгу, которая никогда не воспроизводилась, убедиться, что скорость применена.
