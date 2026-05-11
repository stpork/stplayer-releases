# Release notes — 0.0.60

Release date: 11-May-2026

## English
- Faster, more resilient catalog browsing: when a primary site is slow to respond, the app now races a mirror in parallel and uses whichever returns first.
- Catalog requests recover better from temporary errors: short-lived "not found" or "forbidden" responses from aggregators and CDNs are now retried instead of failing immediately.
- Pull-to-refresh in local-folder libraries now reflects out-of-band changes (folders added, renamed, moved or deleted via a file manager) instead of waiting on the cached view.
- Lower memory footprint over long sessions: previously unbounded internal caches are now bounded, and idle per-source resources are released after a few minutes of inactivity.
- Smoother behavior under system memory pressure — the app trims more aggressively without losing your current screen or causing cold re-fetches when you return to it.
- Resuming a book that was previously left at (or past) the very end no longer hangs on a buffering screen; playback opens cleanly at the start of the track instead.
- The mini progress bar has been polished: the buffered region is now visibly darker and the track sits in the playhead color, making playback progress easier to read at a glance.
- More reliable playback start when launching audio from background or sleep states — fewer silent failures when starting from notifications, widgets or auto-resume.
- Background audio playback for the long-format library source is more dependable; the player now falls back correctly when a stream needs to keep going while the screen is off.
- Sleep timer behavior is unchanged for users, but is now more robust against edge cases at expiry.
- More reliable downloads: better recovery from transient network errors, cleaner cancellation when you back out of a download, and fewer stuck "in progress" states.
- Improved stability when the system shuts down the playback service — fewer rare crashes during app exit.
- Restored compatibility fixes for some sites whose anti-bot checks had regressed in recent versions.

### Behavior changes
- Pull-to-refresh on local-folder libraries now forces a fresh filesystem scan instead of serving the 12-hour cached view.
- Cold-start "resume" no longer attempts to seek to a position at or beyond the end of a track; it restarts the track at the beginning without autoplay.
- Mini progress bar color roles have been swapped: buffered = darker tone, played = accent color.
- Catalog browsing may briefly issue a second request to a mirror when the primary is slow (>1.5s); this is invisible on healthy connections.

### BREAKING CHANGES
None

### Risks / What to test
- Browse and search across all sources, including ones with mirror domains, on both fast and slow networks.
- Pull-to-refresh a local/SAF folder library after adding, renaming, moving or deleting folders from a separate file manager — changes should appear immediately.
- Start playback from notification / widget / auto-resume after the app has been killed; verify audio actually starts.
- Resume a book that was left finished or nearly finished — the player should open at the start of the track without hanging.
- Long browsing session across multiple sources; check that memory usage stays bounded and the app does not get sluggish.
- Trigger system memory pressure (open many other apps) and return — current screen and playback state should be preserved.
- Download books from web and torrent sources; cancel mid-download and re-start; verify no stuck states.
- Visually verify the mini progress bar colors during buffering and active playback.
- Long-format library: start a track and lock the screen — background playback should continue without dropping.

## Русский
# Примечания к выпуску — 0.0.60

Дата выпуска: 11-May-2026

## Русский
- Более быстрый и устойчивый просмотр каталога: если основной сайт отвечает медленно, приложение параллельно обращается к зеркалу и использует тот ответ, который пришёл первым.
- Запросы каталога лучше переживают временные ошибки: краткие ответы «не найдено» или «доступ запрещён» от агрегаторов и CDN теперь повторяются, а не приводят к мгновенной неудаче.
- Жест «потянуть, чтобы обновить» в библиотеках на основе локальных папок теперь отражает изменения, сделанные снаружи (папки добавлены, переименованы, перемещены или удалены через файловый менеджер), вместо показа закэшированного состояния.
- Меньший расход памяти в долгих сессиях: внутренние кэши, ранее не имевшие верхнего предела, теперь ограничены, а простаивающие ресурсы по источникам освобождаются после нескольких минут бездействия.
- Более мягкая реакция на нехватку памяти в системе — приложение агрессивнее очищает ресурсы, не теряя текущий экран и не вызывая «холодных» перезагрузок при возврате.
- Возобновление книги, оставленной в самом конце (или за ним), больше не зависает на экране буферизации; воспроизведение корректно открывается с начала дорожки.
- Мини-полоса прогресса доработана: область буферизации теперь заметно темнее, а воспроизведённая часть окрашена в цвет указателя — прогресс читается с одного взгляда.
- Более надёжный запуск воспроизведения из фона или из спящих состояний — меньше «тихих» отказов при запуске из уведомлений, виджетов или автовозобновления.
- Фоновое воспроизведение для источника с длинными форматами стало стабильнее; плеер корректнее переключается на запасной путь, когда поток должен продолжаться при выключенном экране.
- Поведение таймера сна для пользователя не меняется, но стало устойчивее в граничных ситуациях по истечении времени.
- Более надёжные загрузки: лучшее восстановление после временных сетевых ошибок, аккуратная отмена при выходе из загрузки и меньше «зависших» состояний.
- Повышена стабильность при остановке службы воспроизведения системой — меньше редких сбоев при выходе из приложения.
- Восстановлены исправления совместимости с рядом сайтов, чьи защиты от ботов недавно начали ломать работу.

### Изменения в поведении
- Жест «потянуть, чтобы обновить» в локальных библиотеках теперь принудительно перечитывает файловую систему вместо показа 12-часового кэша.
- Возобновление при холодном старте больше не пытается перейти к позиции в конце или за концом дорожки; вместо этого дорожка стартует с начала без автоматического воспроизведения.
- Цвета мини-полосы прогресса поменялись ролями: буферизованное — более тёмный оттенок, прослушанное — акцентный цвет.
- При просмотре каталога возможен дополнительный короткий запрос к зеркалу, если основной сайт отвечает дольше 1,5 секунды; на здоровых соединениях это незаметно.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
Отсутствуют

### Риски / Что протестировать
- Просмотр и поиск во всех источниках, включая источники с зеркалами, на быстрых и медленных сетях.
- «Потянуть, чтобы обновить» в локальной/SAF библиотеке после добавления, переименования, перемещения или удаления папок через сторонний файловый менеджер — изменения должны появиться сразу.
- Запуск воспроизведения из уведомления / виджета / автовозобновления после того, как приложение было закрыто системой; убедиться, что звук действительно стартует.
- Возобновление книги, оставленной в конце или почти в конце — плеер должен открыть дорожку с начала без зависания.
- Длительная сессия просмотра по нескольким источникам; проверить, что расход памяти остаётся ограниченным и приложение не «тяжелеет».
- Спровоцировать нехватку памяти (открыть много других приложений) и вернуться — текущий экран и состояние воспроизведения должны сохраниться.
- Загрузка книг из веб- и торрент-источников; отмена в середине и повторный запуск; убедиться, что нет «зависших» состояний.
- Визуально проверить цвета мини-полосы прогресса при буферизации и активном воспроизведении.
- Источник с длинными форматами: запустить дорожку и заблокировать экран — фоновое воспроизведение должно продолжаться без обрыва.
