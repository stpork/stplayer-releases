# Release notes — 0.0.37

Release date: 24-Mar-2026 

## English
- Added LoyalBooks to the built-in catalog, with Top 100 and genre browsing for public-domain audiobooks in English.
- Added Bibe to the built-in catalog for Russian classic audiobooks.
- Added AKnigi24 support for users with access to the extended catalog, including browsing by genre, author, and narrator, plus chapter-based playback and downloads.
- Playback is more reliable on several supported websites that use more complex chapter playlist pages.
- Some Digitalbook and similar web titles with spaces in their links now save to history and reopen or resume more reliably.
- Browsing stays smoother when a cover image fails to load.

### Behavior changes
- AKnigi24 books now open in the app as chapter lists instead of a single archive-style item.
- Web titles whose links contain spaces are now treated more like normal library and history items, so reopen and resume work more consistently.

### BREAKING CHANGES
None

### Risks / What to test
- Browse LoyalBooks and Bibe, open several books, and start playback.
- If you use the extended catalog, open AKnigi24, browse by genre, author, and narrator, then play and download a book.
- Retry books that previously failed to show a full chapter list or had unreliable playback on supported websites.
- Open a Digitalbook title with spaces in its link, confirm it appears in history, then reopen it and resume playback.

## Русский
- В встроенный каталог добавлен LoyalBooks с разделом Top 100 и навигацией по жанрам для англоязычных аудиокниг из общественного достояния.
- В встроенный каталог добавлен Bibe с русской классикой в формате аудиокниг.
- Добавлена поддержка АКниги24 для пользователей с доступом к расширенному каталогу: доступны разделы по жанрам, авторам и исполнителям, а также по-главное воспроизведение и загрузка.
- На нескольких поддерживаемых сайтах надёжнее работает воспроизведение книг со сложными страницами плейлистов и глав.
- Некоторые книги из Digitalbook и похожих веб-источников, у которых в ссылке есть пробелы, теперь надёжнее попадают в историю и корректнее открываются или продолжаются с нужного места.
- Просмотр каталога остаётся плавнее, если не удалось загрузить обложку.

### Изменения поведения
- Книги из АКниги24 теперь открываются в приложении как список глав, а не как один архивный элемент.
- Веб-книги, в ссылках которых есть пробелы, теперь обрабатываются ближе к обычным элементам библиотеки и истории, поэтому повторное открытие и продолжение работают стабильнее.

### Критические изменения
Отсутствуют

### Риски / Что проверить
- Открыть LoyalBooks и Bibe, выбрать несколько книг и проверить запуск воспроизведения.
- Если вы используете расширенный каталог, открыть АКниги24, пройтись по жанрам, авторам и исполнителям, затем проверить воспроизведение и загрузку книги.
- Повторно проверить книги на поддерживаемых сайтах, у которых раньше не показывался полный список глав или нестабильно работало воспроизведение.
- Открыть книгу из Digitalbook со ссылкой, содержащей пробелы, убедиться, что она попадает в историю, затем заново открыть её и проверить продолжение воспроизведения.