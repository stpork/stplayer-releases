# Release notes — 0.0.53

Release date: 14-Apr-2026

## English
- **Proxy support**: added SOCKS5 and HTTP proxy with optional authentication, configurable in Settings. Includes DNS leak protection.
- **Blurred artwork background** on the Player Screen for a more immersive listening experience.
- **Improved media controls**: dynamic media buttons — Previous/Next for multi-track books, ±30s skip for single-track. ±3min seek on all surfaces. Unified 5-button notification layout.
- **Bluetooth & Android Auto metadata**: author and performer now displayed instead of synopsis, Unicode emojis removed from metadata, AVRCP artwork delivered reliably.
- **Cover art quality**: higher resolution artwork across KVH, AKN, LBV, LYB, PLK sources. Unified 512px covers for downloaded books. LibriVox shows full-size covers for 98.5% of books.
- **Smoother category switching**: switching between Audiobooks, Genres, Authors, Performers no longer causes list flickering or redundant network requests. Artwork on media cards stays stable during background metadata loading.
- **IZB source**: Genres, Authors, and Performers categories now work correctly.
- **Sort preferences preserved**: selected sort order and time period persist across app restarts and source switches. Sort checkmarks now display correctly for all sources.
- **Book completion fix**: the "finished" checkmark now clears immediately when restarting a completed book.
- **Torrent download stability**: connection timeouts now show a clear error message instead of silently failing.
- **RuTracker mirrors fix**: mirror list now loads correctly.
- **Sleep timer fade**: smoother perceptual volume fade using cubic curve.
- **Pull-to-refresh stability**: refreshing the book list no longer causes artwork to flash or disappear.
- **ANR fix**: removed blocking call on the main thread during source initialization.
- **Notification artwork fix**: fixed a potential crash when Bluetooth artwork was unavailable.

### Behavior changes
- Default sort period for popularity/rating changed from "All time" to "Today".
- Category dropdown and sort menu are fully independent — changing category preserves your active sort selection.
- Book completion status resets immediately on restart (previously required app restart).

### BREAKING CHANGES
None

### Risks / What to test
- Proxy: test SOCKS5 and HTTP with/without auth, verify no DNS leak.
- Category switching: rapidly switch Audiobooks → Genres → Authors → back, verify no flickering.
- Bluetooth/Android Auto: verify title, author, artwork on car/BT devices.
- Cover art: check quality on Player Screen, Book Screen, notification, BT/AA.
- Sort persistence: set sort to "Popular", close app, reopen — verify restored.
- Sleep timer: verify volume fade sounds smooth.
- IZB: verify Genres, Authors, Performers show items and navigation works.
- Restart a completed book — verify checkmark disappears immediately.

## Русский
- **Поддержка прокси**: SOCKS5 и HTTP прокси с опциональной аутентификацией, настраивается в Настройках. Защита от утечки DNS.
- **Размытый фон обложки** на экране плеера для более погружающего прослушивания.
- **Улучшенное управление воспроизведением**: динамические кнопки — Предыдущий/Следующий для книг с несколькими треками, перемотка ±30с для однотрековых. ±3мин на всех поверхностях. Единый макет уведомления с 5 кнопками.
- **Метаданные Bluetooth и Android Auto**: автор и исполнитель вместо синопсиса, эмодзи убраны, обложки AVRCP доставляются стабильно.
- **Качество обложек**: более высокое разрешение для KVH, AKN, LBV, LYB, PLK. Единые обложки 512px для скачанных книг. LibriVox — полноразмерные обложки для 98.5% книг.
- **Плавное переключение категорий**: переключение Аудиокниги/Жанры/Авторы/Исполнители без мерцания и повторной загрузки. Обложки на карточках стабильны при фоновом обогащении.
- **Источник IZB**: категории Жанры, Авторы и Исполнители теперь работают корректно.
- **Сохранение сортировки**: порядок и период сортировки сохраняются при перезапуске и переключении источников. Галочки сортировки корректны для всех источников.
- **Исправление «прослушано»**: галочка завершения сбрасывается сразу при перезапуске книги.
- **Стабильность торрент-загрузок**: таймауты соединения показывают понятное сообщение об ошибке.
- **Зеркала RuTracker**: список зеркал загружается корректно.
- **Затухание таймера сна**: плавное перцептуальное затухание по кубической кривой.
- **Стабильность pull-to-refresh**: обновление списка без мигания обложек.
- **Исправление ANR**: убран блокирующий вызов на главном потоке.
- **Обложка в уведомлении**: исправлен потенциальный сбой при недоступности Bluetooth-обложки.

### Изменения в поведении
- Период сортировки по умолчанию для популярности/рейтинга изменён с «За всё время» на «Сегодня».
- Выпадающий список категорий и меню сортировки полностью независимы — смена категории сохраняет активную сортировку.
- Статус завершения книги сбрасывается немедленно при перезапуске.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
Нет

### Риски / Что проверить
- Прокси: SOCKS5 и HTTP с аутентификацией и без, проверить отсутствие утечки DNS.
- Переключение категорий: быстро переключаться Аудиокниги → Жанры → Авторы → обратно, без мерцания.
- Bluetooth/Android Auto: название, автор, обложка на автомобильных/BT устройствах.
- Обложки: качество на экране плеера, книги, в уведомлении, BT/AA.
- Сохранение сортировки: установить «Популярные», закрыть, открыть — проверить восстановление.
- Таймер сна: плавное затухание.
- IZB: Жанры, Авторы, Исполнители — навигация работает.
- Перезапустить прослушанную книгу — галочка исчезает сразу.
