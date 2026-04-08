# Release notes — 0.0.17

Release date: 14-Feb-2026 

## English
- Playback is now more resilient when the app is in background or briefly buffering, reducing unexpected stops.
- Resume position is more reliable: older save events no longer overwrite newer listening progress.
- Now-playing metadata updates more consistently during track transitions, reducing stale or missing track details.
- Switching between web, local files, SAF folders, and torrents now keeps playback state aligned more reliably.
- Torrent playback now starts network/session components only when needed and shuts them down when idle, reducing background battery use.
- Overall pause/idle efficiency was improved to reduce unnecessary battery and memory usage.

### Behavior changes
- When paused, the background media service is kept alive for a shorter grace period (about 2 minutes) before stopping if playback is not resumed.
- Play requests from notifications/media controls now get a short startup protection window to avoid premature shutdown during startup.
- The first torrent start in a session may take slightly longer because torrent networking now initializes on demand.

### BREAKING CHANGES
- None

### Risks / What to test
- Start playback from the app, lockscreen, and headset/Bluetooth controls.
- Pause for more than 2 minutes, then resume; verify service/notification behavior and restore position.
- Switch quickly between web/local/SAF/torrent items and verify title/artwork/progress consistency.
- Test weak-network buffering and confirm playback recovers without dropping the session.
- Start torrent playback, stop it, clear torrents, and verify background activity returns to idle.

## Русский
- Воспроизведение стало устойчивее при работе в фоне и кратковременной буферизации: неожиданных остановок стало меньше.
- Точка продолжения стала надежнее: старые события сохранения больше не перезаписывают более свежий прогресс.
- Метаданные текущего трека обновляются стабильнее при переключениях, поэтому реже появляются устаревшие или пустые данные.
- Переключение между web, локальными файлами, SAF-папками и торрентами теперь стабильнее сохраняет корректное состояние плеера.
- Для торрентов сетевые/сессионные компоненты запускаются только по необходимости и останавливаются в простое, что снижает расход батареи в фоне.
- Оптимизирована работа в паузе и простое, чтобы уменьшить лишний расход батареи и памяти.

### Изменения в поведении
- При паузе фоновый медиасервис теперь удерживается меньше по времени (примерно 2 минуты) и затем останавливается, если воспроизведение не возобновили.
- Команды Play из уведомления и медиа-контролов теперь получают короткое окно защиты на старте, чтобы сервис не завершался слишком рано.
- Первый запуск торрента в сессии может занимать немного больше времени, так как торрент-сеть теперь инициализируется по требованию.

### ЛОМАЮЩИЕ ИЗМЕНЕНИЯ
- Нет

### Риски / Что протестировать
- Запуск воспроизведения из приложения, с экрана блокировки и с гарнитуры/Bluetooth-кнопок.
- Пауза более 2 минут и последующее возобновление: проверить поведение сервиса/уведомления и восстановление позиции.
- Быстрые переключения между web/local/SAF/torrent: проверить корректность названия, обложки и прогресса.
- Буферизация при слабой сети: убедиться, что воспроизведение восстанавливается без сброса сессии.
- Запустить торрент, остановить, очистить торренты и проверить, что фоновая активность возвращается к простою.