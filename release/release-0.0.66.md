# Release notes — 0.0.66

Release date: 24-Jun-2026

## English
- **Library data is now protected against silent loss.** The app keeps a sibling backup of your favorites, history and playback session, and automatically restores from it if the main file is ever damaged or truncated. A damaged file is set aside for diagnostics instead of being overwritten with an empty list.
- **Favorites no longer get wiped after a period of disuse.** Read failures on the favorites file now retry up to three times with backoff before giving up, and a transient empty in-memory list can no longer flip your on-disk favorites off.
- **Storage access permission is no longer "lost" after a while.** A short-lived empty system response is no longer mistaken for a revoked folder grant, so users with a custom library folder stop seeing "No media found" after the app has been idle.
- **Custom-folder writes are safer.** When saving to a user-picked folder, the app now keeps a rolling backup of the previous good copy of the library file alongside the main file.
- **Downloads are gated by what the source actually supports.** If a source can't be downloaded from, the download action is blocked everywhere — not just hidden in the menu.
- **Cancelling a download now reliably frees the download slot.** Cancelling no longer leaves the app thinking a download is still in progress, so the next download starts cleanly.
- **Fewer broken-looking pages from anti-scraping sites.** When a site returns an error code but still serves a full page (a common anti-bot trick), the app now parses the page instead of giving up.
- **Better handling of expired or self-signed certificates on third-party mirrors.** Catalog browsing on sites with broken HTTPS no longer hard-fails. (Affects only public catalog/audio fetches; no credentials or personal data are sent through this path.)
- **More stable long browsing sessions.** Reduced memory pressure when switching between many sources during one session — fixes occasional out-of-memory crashes deep into long sweeps.
- **Category pagination on author/genre/performer pages is more reliable.** Pages with empty or malformed link patterns no longer crash mid-scroll, and per-category page size can be tuned per source.
- **Sleeker source switching.** Switching between sources releases idle network connections instead of stockpiling them.
- **Minor catalog tuning across multiple sources** — small fixes to listings, pagination and link patterns so categories and book pages render correctly.

### Behavior changes
- After upgrading, the first save to your library file also creates a `.bak` companion file. If a previous version left your main library file damaged, the app will surface an empty state on first launch and recreate a clean file plus backup on the next save (a `.quarantine` copy of the damaged file is kept for support).
- When a source declares it does not support downloads, the download action is now refused even from deep links / re-invocations, not just hidden in the menu.

### BREAKING CHANGES
- None

### Risks / What to test
- Add/remove favorites, force-stop the app, relaunch — favorites must persist.
- Heavy seek/pause cycles during long playback, then relaunch — playback position and history must survive.
- Pick a custom library folder via the system picker, leave the app idle for hours, return — folder access must still work without re-picking.
- Cancel an in-progress download — starting a new one immediately must work; the app must not report "download already active".
- Browse many sources in one session, including ones with expired certificates or anti-scrape error pages — no crashes, no out-of-memory.
- Open author / genre / performer pages and scroll through several pages — pagination must not stall or crash.
- Try to download from a source marked as non-downloadable — the action must be refused with no side-effects.

## Русский
## Релиз 0.0.66

Дата релиза: 24-Jun-2026

- **Данные библиотеки теперь защищены от тихой потери.** Приложение хранит резервную копию избранного, истории и сессии воспроизведения рядом с основным файлом и автоматически восстанавливается из неё, если основной файл повреждён или обрезан. Повреждённый файл откладывается в сторону для диагностики, а не перезаписывается пустым.
- **Избранное больше не пропадает после долгого простоя.** При ошибке чтения файла избранного выполняется до трёх повторов с нарастающей задержкой; кратковременно пустой список в памяти больше не может стереть избранное на диске.
- **Доступ к выбранной папке больше не «теряется» со временем.** Кратковременный пустой ответ системы больше не воспринимается как отзыв доступа к пользовательской папке — пропадает ситуация «No media found» после долгого простоя.
- **Запись в пользовательскую папку стала безопаснее.** Перед перезаписью основного файла библиотеки в SAF-папке создаётся скользящая резервная копия предыдущей удачной версии.
- **Загрузка ограничивается возможностями источника.** Если источник не поддерживает скачивание, действие блокируется во всех точках входа, а не только скрывается в меню.
- **Отмена загрузки корректно освобождает слот.** После отмены приложение больше не считает, что загрузка ещё идёт, и следующая запускается чисто.
- **Меньше «битых» страниц от сайтов с антибот-защитой.** Если сайт возвращает ошибочный код, но при этом отдаёт полноценную HTML-страницу (типичный антибот-трюк), приложение теперь её разбирает, а не отказывается.
- **Лучше обработка просроченных и самоподписанных сертификатов на сторонних зеркалах.** Просмотр каталога на сайтах с проблемами HTTPS больше не падает жёстко. (Затрагивает только публичные каталоги и аудио; учётные данные и личные данные через этот канал не идут.)
- **Стабильнее длинные сессии просмотра.** Снижено давление на память при переключении между многими источниками за одну сессию — устранены редкие сбои нехватки памяти ближе к концу длинных проходов.
- **Пагинация по автору/жанру/исполнителю стала надёжнее.** Страницы с пустыми или некорректными шаблонами ссылок больше не падают при прокрутке; размер страницы для категорий можно настраивать на уровне источника.
- **Аккуратнее переключение между источниками.** Переход на другой источник освобождает простаивающие сетевые соединения, а не копит их.
- **Мелкая отладка каталогов нескольких источников** — небольшие правки списков, пагинации и шаблонов ссылок для корректного отображения категорий и страниц книг.

### Изменения в поведении
- После обновления первая запись в файл библиотеки создаёт рядом файл `.bak`. Если предыдущая версия оставила основной файл повреждённым, при первом запуске вы увидите пустое состояние, а при следующей записи будут пересозданы и основной файл, и резервная копия (повреждённый файл сохраняется как `.quarantine` для поддержки).
- Если источник декларирует, что не поддерживает скачивание, действие «Скачать» теперь отклоняется даже при вызове через диплинк или повтор — не только скрывается в меню.

### BREAKING CHANGES
- Нет

### Риски / Что протестировать
- Добавить/убрать из избранного, принудительно завершить приложение, перезапустить — избранное должно сохраняться.
- Активные перемотки/паузы во время длинного воспроизведения, затем перезапуск — позиция и история должны выживать.
- Выбрать пользовательскую папку библиотеки через системный пикер, оставить приложение в покое на несколько часов, вернуться — доступ к папке должен работать без повторного выбора.
- Отменить идущую загрузку — следующая загрузка должна стартовать сразу; не должно быть «загрузка уже активна».
- Просмотреть много источников за одну сессию, в том числе с истёкшими сертификатами и антибот-страницами ошибок — без падений и нехватки памяти.
- Открыть страницы автора/жанра/исполнителя и прокрутить несколько страниц — пагинация не должна зависать или падать.
- Попытаться скачать из источника, помеченного как не поддерживающий скачивание, — действие должно быть отклонено без побочных эффектов.
