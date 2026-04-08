# Release notes — 0.0.36

Release date: 20-Mar-2026 

## English
- Patephone playback is more reliable for books opened from newer link formats, reducing cases where playback fails to start.
- LibriVox books hosted on archive.org now start more reliably.
- Digitalbook.io titles now load fuller book details in the background, with better duration data for tracks and books.
- Problematic online books are less likely to trigger repeated background retries in the same session, which helps keep browsing smoother when a source is having trouble.
- Sources with only one category no longer show a redundant category picker.

### Behavior changes
- Sources with one category now open without a one-item category selector in the top bar.
- If an online item fails background detail loading several times in one session, the app stops retrying it until the next app launch.

### BREAKING CHANGES
None

### Risks / What to test
- Open and play several Patephone books, including items reached from search and direct book pages.
- Play several LibriVox books and confirm archive.org-hosted audio starts normally.
- Browse Digitalbook.io and confirm descriptions, narrators, genres, and durations fill in after the list loads.
- Check sources with a single category and confirm the redundant category picker is gone.

## Русский
- В Патефоне надёжнее запускается воспроизведение книг, открытых по новым форматам ссылок, поэтому случаев, когда книга не стартует, стало меньше.
- Книги из LibriVox, размещённые на archive.org, теперь запускаются надёжнее.
- Для Digitalbook.io теперь в фоне подгружаются более полные сведения о книгах, а данные о длительности треков и книг стали точнее.
- Проблемные онлайн-книги теперь реже вызывают повторяющиеся фоновые попытки загрузки в рамках одной сессии, поэтому просмотр остаётся плавнее, если источник работает нестабильно.
- Для источников только с одной категорией больше не показывается лишний переключатель категории.

### Изменения поведения
- Источники с одной категорией теперь открываются без селектора с единственным пунктом в верхней панели.
- Если у онлайн-элемента несколько раз подряд не удаётся фоновая загрузка сведений в рамках одной сессии, приложение прекращает повторные попытки до следующего запуска.

### Критические изменения
Отсутствуют

### Риски / Что проверить
- Открыть и запустить несколько книг из Патефона, включая результаты поиска и прямые страницы книг.
- Запустить несколько книг из LibriVox и проверить, что аудио с archive.org стартует нормально.
- Открыть Digitalbook.io и проверить, что после загрузки списка подтягиваются описания, чтецы, жанры и длительность.
- Проверить источники с одной категорией и убедиться, что лишний переключатель категории исчез.