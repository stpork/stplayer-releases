# Release notes — 0.0.44

Release date: 01-Apr-2026 

## English
- Android Auto browsing has been reorganized around a single `Sources` entry that follows the same tab order and visibility as the main library.
- Android Auto source pages now surface filters such as sort options and categories before the main book list, making deep browsing faster.
- Cover art now appears more reliably for local folders, downloads, and other private files in notifications, Android Auto, and other external playback surfaces.
- Local history and library entries now detect folder cover images more accurately, reducing missing or wrong artwork for on-device books.
- Fixed duplicate starts from repeated headset and media-button signals, reducing accidental double launches and repeated resumes.
- Notification and other in-app playback actions now wake the player more reliably when commands arrive from the background.
- Opening a source now lands on its intended default feed or sort more consistently, especially for sources with category-based browsing.

### Behavior changes
- Android Auto home now opens through `Sources` instead of several separate top-level shortcuts.
- Enabled tabs and sources in Android Auto now follow the same order and visibility settings as the main library.
- When a source offers extra browse options, Android Auto shows a `Filters` entry before the default book list.
- Private and local cover art may now be shown on system playback surfaces instead of appearing blank.

### BREAKING CHANGES
- None

### Risks / What to test
- Android Auto: open `Sources`, check tab order, open filters and categories, and start a book.
- Headset, Bluetooth, and media buttons: start playback from a stopped app and confirm only one launch happens.
- Notifications: use play, pause, next, previous, and stop after the app has been in the background.
- Local folders, downloads, history, and favorites: confirm cover art appears correctly in the player, notification, and Android Auto.
- Open several sources and confirm the first feed shown matches the expected default.

## Русский
- Навигация в Android Auto теперь строится вокруг единого раздела `Источники`, который повторяет порядок и видимость вкладок из основной библиотеки.
- На страницах источников в Android Auto теперь сначала показываются фильтры, например сортировка и категории, а уже потом основной список книг, поэтому до нужного раздела добираться быстрее.
- Обложки теперь надежнее отображаются для локальных папок, загрузок и других непубличных файлов в уведомлениях, Android Auto и на других внешних поверхностях управления воспроизведением.
- Локальная история и элементы библиотеки теперь точнее находят обложки папок, поэтому для книг на устройстве реже пропадает или подменяется изображение обложки.
- Исправлен повторный запуск из-за серии сигналов от гарнитуры и медиа-кнопок: стало меньше случайных двойных запусков и повторных восстановлений.
- Действия воспроизведения из уведомлений и других внутренних элементов управления теперь надежнее пробуждают плеер, когда команда приходит в фоне.
- При открытии источника теперь чаще сразу показывается правильная стартовая лента или сортировка, особенно у источников с просмотром по категориям.

### Изменения поведения
- Главный экран Android Auto теперь открывается через раздел `Источники`, а не через несколько отдельных верхнеуровневых ярлыков.
- Включенные вкладки и источники в Android Auto теперь идут в том же порядке и с той же видимостью, что и в основной библиотеке.
- Если у источника есть дополнительные варианты просмотра, в Android Auto перед списком книг теперь показывается пункт `Фильтры`.
- Обложки из приватного и локального хранилища теперь могут отображаться на системных поверхностях воспроизведения вместо пустых изображений.

### Несовместимые изменения
- Нет

### Риски / Что проверить
- Android Auto: откройте `Источники`, проверьте порядок вкладок, откройте фильтры и категории, затем запустите книгу.
- Гарнитура, Bluetooth и медиа-кнопки: запустите воспроизведение из полностью остановленного приложения и убедитесь, что запуск происходит только один раз.
- Уведомления: проверьте команды воспроизведения, паузы, следующего, предыдущего трека и остановки после работы приложения в фоне.
- Локальные папки, загрузки, история и избранное: убедитесь, что обложки правильно показываются в плеере, уведомлении и Android Auto.
- Откройте несколько источников и проверьте, что первым показывается ожидаемый стартовый список.