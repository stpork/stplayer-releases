# Release notes — 0.0.58

Release date: 27-Apr-2026

## English
- Sleep timer: smoother slider control with a wider, more useful motion-reset sensitivity range (2–8 g, default 2.5 g) so a tap or shake reliably keeps playback alive without false triggers.
- Better battery life during playback: fewer redundant foreground notifications, no leaked wake locks on cancel, less vibrator/timer chatter in the background.
- Fixed an issue where stopping a torrent stream could race with cleanup and occasionally leave the player in a stuck state.
- Library drawer no longer auto-closes unexpectedly during open/close animations.
- Cold start is faster: session restore work now runs off the main thread, so the first screen appears sooner.
- Eliminated phantom “save failed / persist failed” log noise that appeared during normal source switching, cover loading, scraping, and downloads.
- Fixed a torrent file reader bug that could spin in an infinite loop or silently swallow read errors during playback.
- Pausing background network activity (e.g. when the app is backgrounded or sources switch) now actually pauses the request queue instead of cancelling it, preventing a flood of redundant network requests when you come back.
- Fixed a rare metadata cache reading bug that could misinterpret stored format versions.

### Behavior changes
- Default motion-reset sensitivity for the sleep timer changed to 2.5 g; previously saved custom values are preserved.
- Resuming after the app pauses background work returns much faster — queued items resume instead of being rebuilt from scratch.

### BREAKING CHANGES
- None

### Risks / What to test
- Sleep timer: tap-to-extend and motion-reset behavior across the full slider range.
- Torrent playback: start, stop, and switch between torrents; verify nothing remains running after Stop.
- Library drawer: open/close, swipes, and rapid taps during animation.
- Cold start with a previous session: app should open quickly and resume the last book/position.
- Backgrounding and resuming the app while scraping/loading; verify lists and covers continue without re-fetching everything.
- Long playback sessions: confirm battery drain is in line with or better than 0.0.57.
- Downloads, cover loading, and source switching: no spurious error toasts or log spam.

## Русский
- Таймер сна: более плавный слайдер и расширенный, более удобный диапазон чувствительности к движению (2–8 g, по умолчанию 2.5 g) — лёгкое касание или встряхивание надёжно продлевают воспроизведение без ложных срабатываний.
- Меньший расход батареи при воспроизведении: убраны лишние повторные уведомления службы, исправлены утечки wake-lock при отмене, снижена частота тиков таймера и вибраций в фоне.
- Исправлена ошибка, при которой остановка торрент-потока могла конфликтовать с очисткой и иногда оставляла плеер в зависшем состоянии.
- Боковая панель библиотеки больше не закрывается сама во время анимации открытия/закрытия.
- Холодный старт стал быстрее: восстановление сессии теперь выполняется вне основного потока, и первый экран появляется заметно раньше.
- Убран фантомный шум вида «save failed / persist failed» в логах, появлявшийся при обычной смене источника, загрузке обложек, парсинге и скачивании.
- Исправлена ошибка чтения торрент-файла, из-за которой мог происходить бесконечный цикл или скрытое игнорирование ошибок ввода-вывода во время воспроизведения.
- Пауза фоновой сетевой активности (например, при сворачивании приложения или переключении источников) теперь действительно ставит очередь запросов на паузу, а не отменяет её — это предотвращает шквал повторных запросов при возврате.
- Исправлена редкая ошибка чтения кэша метаданных, из-за которой мог неверно интерпретироваться номер версии формата.

### Изменения в поведении
- Значение по умолчанию для чувствительности таймера сна изменено на 2.5 g; ранее сохранённые пользовательские значения не затронуты.
- Возврат после паузы фоновой работы происходит существенно быстрее — элементы очереди возобновляются, а не пересоздаются заново.

### BREAKING CHANGES
- Нет

### Риски / Что протестировать
- Таймер сна: продление касанием и сброс по движению во всём диапазоне слайдера.
- Воспроизведение торрентов: запуск, остановка и переключение между торрентами; убедиться, что после Stop ничего не остаётся работать.
- Боковая панель библиотеки: открытие/закрытие, свайпы и быстрые касания во время анимации.
- Холодный старт с прошлой сессией: приложение должно открываться быстро и возобновлять последнюю книгу с нужной позиции.
- Сворачивание и возврат приложения во время парсинга/загрузки; убедиться, что списки и обложки продолжают работу без полной перезагрузки.
- Длительные сеансы воспроизведения: проверить, что расход батареи не хуже, чем в 0.0.57.
- Загрузки, подгрузка обложек и переключение источников: отсутствие ложных сообщений об ошибках и шума в логах.
