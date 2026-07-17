I have the commit list, diff stats, and name-status — which is enough to identify all user-facing changes. The remaining lines are diff detail I don't need for user-facing notes. Let me generate the release notes.

# Release notes — 0.0.71

Release date: 17-Jul-2026

## English
- **Playback resumes reliably after the app is closed or the device reboots.** Your position, speed and pitch are now saved the moment you pause or stop, so you pick up exactly where you left off — even after a force-stop or restart.
- **Streaming keeps playing when an access link expires.** If a stream's authentication token times out mid-listen, the app now quietly refreshes it and continues instead of dropping into an error.
- **Resuming a book from history no longer fails to start.** Fixed a case where playback would stall or error when reopening certain streamed titles from your history.
- **Maximum playback speed raised to 3.0×** (previously 2.0×).
- **Artwork tap and long-press now act on the book that's actually playing.** Tapping the cover switches between the player and book detail; a long-press anywhere on an item opens its context menu.
- **Reviews are back for providers that show them** — a bug that had broken review loading across the board is fixed.
- **Category lists (authors, genres, performers) open correctly** and show a compact, tappable layout on every provider, instead of "No media found" or broken chips.
- **Search is more resilient to rate-limiting** — an empty result caused by throttling is now retried automatically instead of showing nothing.
- **Book durations fill in more completely** for library items that were missing them.
- **Downloads got safer and clearer:** corrupt downloads are detected and cleaned up automatically, deleting a downloaded book now removes it fully so it doesn't reappear, and a track whose link expired mid-download is retried with a fresh link instead of failing the whole book.
- **Better car and Bluetooth playback:** cover art now shows for all external players (not just Android Auto), the browse view uses a cleaner grid layout, and the library is searchable from the car.
- **Longer battery life during sleep-timer and idle playback** thanks to reduced background polling.
- **More complete and corrected translations** across all supported languages, including book-detail labels, error messages and the speed dialog buttons.
- **Security & stability:** plain-text (unencrypted) web traffic is now disabled app-wide, sensitive tokens are no longer written to logs, and several rare crashes were fixed.

### Behavior changes
- Pausing or stopping now saves your position immediately (previously it could be saved on a delay), so resume is more accurate.
- Long-press to open the context menu is unified to a consistent ~0.6s hold and no longer triggers accidentally while scrolling.
- Tapping the cover art now toggles between the player and book screen for the currently playing book.
- Expired streaming sessions are refreshed automatically rather than surfacing a network error.

### BREAKING CHANGES
- None.

### Risks / What to test
- Resume after pause/stop, after force-stop, and after a reboot — verify position, speed and pitch are restored.
- Long-listening on streamed providers — confirm playback continues past token/link expiry without an error.
- Opening books from history and reopening recently played titles.
- Author / genre / performer category lists across several providers — confirm they open and are tappable.
- Search under repeated queries — confirm throttled empty results recover.
- Download a book, delete it, and confirm it's fully gone; download a large book and confirm expired-link retry.
- Car / Bluetooth playback — cover art, browsing and search.
- Playback speed up to 3.0×.
- Spot-check translations in a couple of languages (book detail, error toasts, speed dialog).

## Русский

## Русский
- **Воспроизведение надёжно возобновляется после закрытия приложения или перезагрузки устройства.** Позиция, скорость и высота тона теперь сохраняются в момент паузы или остановки, поэтому вы продолжаете ровно с того места, где остановились — даже после принудительного закрытия или перезагрузки.
- **Потоковое воспроизведение продолжается при истечении срока действия ссылки доступа.** Если токен авторизации потока истекает во время прослушивания, приложение теперь незаметно обновляет его и продолжает играть, а не выдаёт ошибку.
- **Возобновление книги из истории больше не даёт сбой при запуске.** Исправлен случай, когда воспроизведение зависало или выдавало ошибку при повторном открытии некоторых потоковых книг из истории.
- **Максимальная скорость воспроизведения повышена до 3.0×** (ранее 2.0×).
- **Нажатие и долгое нажатие на обложку теперь работают с той книгой, которая реально играет.** Нажатие на обложку переключает между плеером и деталями книги; долгое нажатие в любом месте элемента открывает его контекстное меню.
- **Отзывы снова работают у провайдеров, которые их показывают** — исправлена ошибка, из-за которой загрузка отзывов была сломана повсеместно.
- **Списки категорий (авторы, жанры, чтецы) открываются корректно** и показывают компактный, нажимаемый вид у каждого провайдера, вместо «Ничего не найдено» или сломанных элементов.
- **Поиск устойчивее к ограничению частоты запросов** — пустой результат из-за троттлинга теперь автоматически повторяется, а не показывает пустоту.
- **Длительность книг заполняется полнее** для элементов библиотеки, у которых её не хватало.
- **Загрузки стали безопаснее и понятнее:** повреждённые загрузки обнаруживаются и очищаются автоматически, удаление скачанной книги теперь удаляет её полностью, чтобы она не появлялась снова, а трек с истёкшей ссылкой во время загрузки повторяется со свежей ссылкой вместо провала всей книги.
- **Улучшено воспроизведение в авто и по Bluetooth:** обложки теперь показываются для всех внешних плееров (не только Android Auto), режим обзора использует более аккуратную сетку, а библиотека доступна для поиска из автомобиля.
- **Дольше держит батарея при таймере сна и в простое** за счёт уменьшения фоновых опросов.
- **Более полные и исправленные переводы** на всех поддерживаемых языках, включая подписи в деталях книги, сообщения об ошибках и кнопки диалога скорости.
- **Безопасность и стабильность:** незашифрованный (plain-text) веб-трафик теперь отключён во всём приложении, конфиденциальные токены больше не пишутся в логи, а также исправлено несколько редких сбоев.

### Изменения в поведении
- Пауза или остановка теперь сохраняют позицию сразу (раньше могло сохраняться с задержкой), поэтому возобновление точнее.
- Долгое нажатие для вызова контекстного меню унифицировано до постоянного удержания ~0.6с и больше не срабатывает случайно при прокрутке.
- Нажатие на обложку теперь переключает между экраном плеера и книги для текущей играющей книги.
- Истёкшие потоковые сессии обновляются автоматически, а не показывают сетевую ошибку.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
- Нет.

### Риски / Что проверить
- Возобновление после паузы/остановки, после принудительного закрытия и после перезагрузки — проверить восстановление позиции, скорости и высоты тона.
- Долгое прослушивание у потоковых провайдеров — убедиться, что воспроизведение продолжается после истечения токена/ссылки без ошибки.
- Открытие книг из истории и повторное открытие недавно проигранных книг.
- Списки категорий авторов / жанров / чтецов у нескольких провайдеров — убедиться, что они открываются и нажимаются.
- Поиск при повторяющихся запросах — убедиться, что пустые результаты из-за троттлинга восстанавливаются.
- Скачать книгу, удалить её и убедиться, что она удалена полностью; скачать большую книгу и проверить повтор при истёкшей ссылке.
- Воспроизведение в авто / по Bluetooth — обложки, обзор и поиск.
- Скорость воспроизведения до 3.0×.
- Выборочно проверить переводы на паре языков (детали книги, всплывающие ошибки, диалог скорости).
