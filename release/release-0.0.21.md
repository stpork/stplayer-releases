# Release notes — 0.0.21

Release date: 19-Feb-2026 

## English
- Improved YouTube browsing reliability: pagination and infinite scroll now return content more consistently instead of stopping early or showing empty steps.
- Improved YouTube playback stability: fewer failed starts and fewer client/session-related playback errors during normal use.
- Added multi-audio support for YouTube content, including language-aware track switching and clearer active-track display in Mini Player and Player.
- Fixed metadata mix-ups where language labels could overwrite creator/author text.
- Improved startup and library restore behavior so the app more reliably returns to the expected source/view state.
- Reduced background activity and tuned metadata update batching to improve responsiveness and lower unnecessary background churn.
- Updated key player/list UI details (title wrapping and compact list/file picker behavior) for better readability on real devices.

### Behavior changes
- YouTube discovery continues to use a browsing path optimized for stable pagination, while playback uses a path optimized for playable streams.
- When YouTube items have multiple audio tracks, the selected language/track is now visible and switchable in playback UI.
- Startup/source restoration is more deterministic, reducing unexpected landing states.

### BREAKING CHANGES
- None

### Risks / What to test
- YouTube search/category scrolling across multiple pages.
- Start playback from search results and playlists, then skip between items.
- Multi-audio switching (language changes) in Mini Player and full Player.
- App restart and source/view restoration flow.
- Background/foreground transitions and playback position persistence.

## Русский
- Повышена надежность просмотра YouTube: пагинация и бесконечная прокрутка теперь стабильнее возвращают контент и реже останавливаются или показывают пустые шаги.
- Улучшена стабильность воспроизведения YouTube: меньше неудачных стартов и ошибок, связанных с клиентом/сессией, в обычных сценариях.
- Добавлена поддержка нескольких аудиодорожек для YouTube, включая переключение языков и более понятное отображение активной дорожки в Mini Player и Player.
- Исправлены ошибки метаданных, из-за которых подписи языков могли перезаписывать имя автора/исполнителя.
- Улучшено поведение при запуске и восстановлении библиотеки: приложение надежнее возвращается в ожидаемый источник/экран.
- Снижена фоновая нагрузка и оптимизировано пакетное обновление метаданных для лучшей отзывчивости и меньшей лишней активности в фоне.
- Обновлены важные UI-детали плеера и списков (перенос заголовков, компактное поведение списков/файлового диалога) для лучшей читаемости на устройствах.

### Behavior changes
- Для YouTube путь поиска/просмотра по-прежнему оптимизирован под стабильную пагинацию, а путь воспроизведения — под более надежные проигрываемые потоки.
- Если у YouTube-элемента несколько аудиодорожек, выбранный язык/дорожка теперь виден и переключается в интерфейсе воспроизведения.
- Восстановление состояния при запуске и возврат к источнику стали более предсказуемыми.

### BREAKING CHANGES
- None

### Risks / What to test
- Прокрутка YouTube-поиска/категорий через несколько страниц.
- Запуск воспроизведения из результатов поиска и плейлистов, переключение между треками.
- Переключение нескольких аудиодорожек (смена языка) в Mini Player и полном Player.
- Перезапуск приложения и восстановление источника/экрана.
- Переходы фон/передний план и сохранение позиции воспроизведения.