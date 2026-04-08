# Release notes — 0.0.5

Release date: 09-Feb-2026

## English
- Added a new **Download folder access check** in Settings, with clear status (“configured”, “not configured”, or “access blocked”).
- Download folder setup is now validated more strictly before saving, which prevents failed downloads caused by invalid or restricted folder selections.
- When folder access fails, the app now shows a clear recovery dialog with direct actions to pick another folder or open app permissions.
- Improved media controls in notifications/system player: controls now adapt to content type (chapter navigation for multi-track books, 30-second seek for single-track audio), plus a dedicated Stop action.
- Fixed an issue where pause from system controls could be undone by unwanted auto-resume behavior.
- Improved playback startup smoothness by moving heavy playlist preparation off the main UI thread.
- Improved History/Favorites/Library responsiveness with more efficient list/state updates, especially on larger libraries.

### Behavior changes
- Tapping the system media notification now opens the player more reliably for the currently relevant book.
- Notification/media-panel controls are now context-aware (Previous/Next for multi-track, Rewind/Forward 30s for single-track).
- Dismissing the media notification now acts as a full terminate action (playback stops and the app session ends).

### BREAKING CHANGES
- Dismissing the media notification now fully ends the app session instead of only hiding controls.

### Risks / What to test
- Verify download folder selection, re-check, and permission recovery flow on real devices.
- Verify notification controls for both single-track and multi-track books (play/pause/seek/next/previous/stop).
- Verify external pause commands (Bluetooth/headset/system mini player) do not auto-resume unexpectedly.
- Verify notification tap always opens the correct player context.
- Verify app behavior after dismissing the media notification matches expected terminate flow.

## Русский
- В настройках добавлена новая проверка доступа к папке загрузок с понятным статусом («настроено», «не настроено» или «доступ заблокирован»).
- Настройка папки загрузок теперь проверяется строже до сохранения, что предотвращает сбои загрузки из-за неверно выбранной или ограниченной папки.
- При проблемах с доступом к папке приложение теперь показывает понятный диалог восстановления с быстрыми действиями: выбрать другую папку или открыть разрешения приложения.
- Улучшены элементы управления в уведомлении/системном плеере: кнопки теперь зависят от типа контента (переключение треков для многотрековых книг, перемотка на 30 секунд для однотрекового аудио), добавлена отдельная кнопка Stop.
- Исправлена проблема, при которой пауза из системных элементов управления могла отменяться нежелательным авто-возобновлением.
- Повышена плавность запуска воспроизведения: тяжелая подготовка плейлиста перенесена с главного UI-потока.
- Улучшена отзывчивость экранов Истории/Избранного/Библиотеки за счет более эффективных обновлений списков и состояния, особенно на больших библиотеках.

### Behavior changes
- Нажатие на системное медиа-уведомление теперь надежнее открывает плеер для актуальной книги.
- Кнопки в уведомлении/медиапанели теперь контекстные (Previous/Next для многотрекового контента, Rewind/Forward на 30 секунд для однотрекового).
- Смахивание медиа-уведомления теперь выполняет полное завершение сессии (воспроизведение останавливается, сессия приложения завершается).

### BREAKING CHANGES
- Смахивание медиа-уведомления теперь полностью завершает сессию приложения, а не просто скрывает элементы управления.

### Risks / What to test
- Проверьте выбор папки загрузок, повторную проверку доступа и восстановление через разрешения на реальных устройствах.
- Проверьте кнопки уведомления для однотрековых и многотрековых книг (play/pause/seek/next/previous/stop).
- Проверьте, что внешняя пауза (Bluetooth/гарнитура/системный мини-плеер) больше не вызывает неожиданное авто-возобновление.
- Проверьте, что нажатие на уведомление всегда открывает правильный контекст плеера.
- Проверьте, что поведение после смахивания медиа-уведомления соответствует ожидаемому сценарию завершения.