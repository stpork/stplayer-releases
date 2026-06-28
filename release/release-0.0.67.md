# Release notes — 0.0.67

Release date: 29-Jun-2026

## English
- New downloads for one of the supported sources now unpack their archive contents directly into your library, so multi-track books arrive ready to play instead of as a single bundle.
- Downloads use the same network identity as playback (referer, user agent, cookies), fixing failures where some sources rejected downloads even though streaming worked.
- "Partial download" books in your library now show an in-progress badge and never claim "Complete" until every track is on disk.
- The downloaded badge survives clearing app data and cold launches, so previously downloaded books stay recognizable after a reinstall.
- Cancelling a download mid-flight now stops cleanly and atomically, with no stuck "completing" state and no leftover partial files.
- Favorites load on app start, so the first time you toggle a favorite the count no longer jumps from 0 to N.
- Switching between sources no longer leaks state from the previous source into the new one.
- One source's playlist filter has been updated so playlist-only filtering works again; another source now retries playlists and presents itself correctly to upstream servers.
- One source's top-rated sort and another source's signed-track URLs both work again after upstream changes.
- The media notification is more reliable: the artwork updates consistently, the notification no longer goes blank intermittently, and it no longer disappears on certain manufacturer ROMs.
- HLS-style downloads no longer cause memory pressure on books with very long chapters.
- Per-track storage checks no longer over-count free-space requirements, so legitimate downloads are no longer blocked by phantom "not enough space" errors.
- Storage permissions: the misleading "All files" hint was removed, and the granted folder now persists correctly on first acceptance.
- On Xiaomi/MIUI devices, downloads no longer create a confusing nested "Downloads" folder inside the system Downloads tree.
- Improved overall stability: fixed a crash during secure connections to certain sites, and reduced memory spikes when parsing very large pages.

### Behavior changes
- Downloads now stream the same headers, cookies, and user agent as the player, which may change how some upstream sites see download traffic compared to before.
- After granting storage access, the chosen folder is treated as a single app-wide media root.
- Book detail refresh waits longer (up to 10s) for slower sources before giving up.

### BREAKING CHANGES
- None

### Risks / What to test
- Start, pause, resume, and cancel a download; confirm the file is finalized or cleanly removed.
- Re-open the app after a download completes; the downloaded badge should still appear.
- Clear app data, reinstall, and re-grant the storage folder; previously downloaded books should reappear.
- Toggle a favorite on a fresh launch; confirm the count is correct from the first tap.
- Switch between sources and verify lists, search, and badges reflect the active source only.
- Play a track and observe the lockscreen/notification: artwork visible, controls responsive, no flicker.
- On Xiaomi/MIUI and Android 12+ devices, confirm downloads land in the expected folder and the foreground notification stays visible.

## Русский
- Загрузки одного из поддерживаемых источников теперь автоматически распаковывают архив в библиотеку — многотрековые книги сразу готовы к воспроизведению, а не лежат единым файлом.
- Загрузка использует те же сетевые заголовки, что и воспроизведение (referer, user-agent, cookies). Это устраняет случаи, когда стриминг работал, а скачивание отклонялось.
- Книги с частичной загрузкой в библиотеке корректно показывают значок «в процессе» и больше не помечаются как «Завершено» до фактической загрузки всех треков.
- Значок «загружено» сохраняется после очистки данных приложения и холодного старта — ранее скачанные книги остаются опознанными даже после переустановки.
- Отмена загрузки на середине теперь срабатывает чисто и атомарно: нет «зависшего» состояния завершения и нет недокачанных огрызков на диске.
- Избранное загружается при старте приложения — счётчик при первом нажатии больше не прыгает с 0 на N.
- Переключение между источниками больше не оставляет «хвостов» предыдущего источника в новом.
- У одного источника обновлён фильтр «только плейлисты»; другой теперь повторно запрашивает плейлисты и корректно представляется серверу.
- У одного источника снова работает сортировка по рейтингу, у другого — корректно подписываются ссылки на треки.
- Уведомление плеера стало надёжнее: обложка обновляется стабильно, уведомление перестало периодически пропадать и больше не теряется на некоторых прошивках производителей.
- Загрузки в формате HLS больше не давят на память при книгах с очень длинными главами.
- Проверка свободного места перед загрузкой больше не завышает требуемый объём — корректные загрузки больше не блокируются ложной нехваткой места.
- Доступ к хранилищу: убрана вводящая в заблуждение подсказка «Все файлы», а выбранная папка стабильно сохраняется с первого согласия.
- На устройствах Xiaomi/MIUI загрузки больше не создают вложенную папку «Downloads» внутри системной папки «Загрузки».
- Общая стабильность: устранено падение при защищённых соединениях с некоторыми сайтами и снижены пики памяти при парсинге очень больших страниц.

### Изменения в поведении
- При загрузке теперь используются те же заголовки, cookies и user-agent, что и при воспроизведении — для удалённых серверов трафик может выглядеть иначе, чем раньше.
- После выдачи доступа к хранилищу выбранная папка считается единым корневым каталогом мультимедиа для всего приложения.
- Обновление страницы книги ждёт ответа более медленных источников дольше (до 10 секунд).

### BREAKING CHANGES
- Нет

### Риски / Что проверить
- Запуск, пауза, продолжение и отмена загрузки; убедиться, что файл либо корректно завершён, либо чисто удалён.
- Перезапустить приложение после завершения загрузки; значок «загружено» должен сохраниться.
- Очистить данные приложения, переустановить, заново выдать доступ к папке; ранее скачанные книги должны снова появиться.
- Включить избранное при свежем запуске; счётчик должен быть корректен с первого нажатия.
- Переключиться между источниками: списки, поиск и значки должны отражать только текущий источник.
- Воспроизвести трек и проверить уведомление/локскрин: обложка видна, элементы управления отзывчивы, без мерцаний.
- На устройствах Xiaomi/MIUI и Android 12+: убедиться, что загрузки попадают в ожидаемую папку и foreground-уведомление остаётся видимым.
