The remaining content is the truncated diff (mostly help-text translations and internal code). I have the commit list, diff stats, and enough of the diff to identify all user-facing changes. Let me scan the rest quickly for any additional user-visible feature, then write the notes.

The commit list is comprehensive and is the authoritative source for what changed. I have everything I need. Let me synthesize user-facing themes:

**Features:** two-phase Global Search (entities → books, all sources at once, infinite scroll), navigation history stack (Spotify-style back), long-press indicator, local search/filter on History & Favorites, long-press on book category/title → global search, compact view counts (15.9k).

**Fixes/stability:** OOM crashes bounded (artwork memory, HTTP thread pool, HTML parse concurrency), playhead no longer freezes, cold-resume re-applies speed, in-source search pagination on all providers, YouTube session recovery on 403/410, various nav Back fixes, book description/reviews load from global search, swipe-right on favorite opens book.

**UI/UX:** friendlier help (12 languages), complete dark/twilight themes, spinner consistency, startup opens first network source, web-source globe icon.

I'll consolidate and exclude internal work.

# Release notes — 0.0.73

Release date: 25-Jul-2026

## English

- **Redesigned Global Search across all sources at once.** Search for genres, authors, or narrators and get one card per name (merged across sources); tap a card to see all their books. Results now load progressively and keep loading as you scroll.
- **New navigation history.** A Back-stack remembers where you came from, so pressing Back walks you back the exact way you arrived (Player → Book → Search → Category) instead of jumping somewhere unexpected.
- **Search & filter your own lists.** History and Favorites now have a quick filter to narrow your saved books by title, author, or narrator — instantly, without loading anything.
- **Long-press a book's title, author, genre, or narrator** to search every source for that name.
- **Clearer long-press feedback.** A smooth radial indicator shows a long-press building up, and cancels cleanly on release or double-tap.
- **Fewer crashes.** Several out-of-memory crashes (during heavy browsing, cover loading, and busy network activity) have been fixed for a more stable experience on all devices.
- **Smoother playback UI.** The playhead no longer freezes, and resuming a book now correctly restores your chosen playback speed.
- **In-source search now pages through all results** on every catalog, so you're no longer limited to the first page.
- **More reliable YouTube playback**, with automatic recovery and a short rewind when a session needs to refresh.
- **View counts are now compact** (e.g. 15.9k instead of 15,937).
- **Friendlier, rewritten Help** in all 12 languages, plus polished dark and twilight themes.
- **App opens your first online library on launch**, and book details and reviews now load immediately when opened from search.

### Behavior changes

- Pressing Back follows your actual path through the app (reverse-chronological), rather than a fixed screen order.
- Genre/author/narrator cards in Global Search only open book lists — they never start playback.
- Swiping right on a Favorite now opens the Book screen.
- In-source search loads more results as you scroll instead of stopping at the first page.

### BREAKING CHANGES

- None

### Risks / What to test

- Global Search: entity cards (genre/author/narrator), tapping into a card's book list, infinite scroll, and Back from results.
- Back navigation across chains (Player → Book → Search → Category → Library) and after switching sources.
- Playback: resume restores speed and position; playhead keeps advancing; skip-silence and normalization.
- Long-press on books and on book title/author/genre; long-press indicator cancel on release/double-tap.
- History & Favorites local filter; swipe-left to delete; swipe-right on a Favorite opens the book.
- Downloads, offline playback, and download pause/resume/cancel.
- Stability under heavy browsing and many covers loading (no crashes).
- Help screen and theme rendering in dark/twilight across languages.

## Русский

- **Переработанный глобальный поиск сразу по всем источникам.** Ищите жанры, авторов или чтецов и получайте по одной карточке на имя (объединённой между источниками); нажмите карточку, чтобы увидеть все их книги. Результаты теперь подгружаются постепенно и продолжают загружаться при прокрутке.
- **Новая история навигации.** Стек «Назад» запоминает, откуда вы пришли, поэтому кнопка «Назад» ведёт вас ровно тем путём, которым вы шли (Плеер → Книга → Поиск → Категория), а не перекидывает в неожиданное место.
- **Поиск и фильтр по вашим спискам.** В «Истории» и «Избранном» появился быстрый фильтр, чтобы мгновенно сузить сохранённые книги по названию, автору или чтецу — без какой-либо загрузки.
- **Долгое нажатие на название книги, автора, жанр или чтеца** запускает поиск этого имени по всем источникам.
- **Понятнее отклик на долгое нажатие.** Плавный радиальный индикатор показывает, что долгое нажатие набирается, и аккуратно отменяется при отпускании или двойном касании.
- **Меньше сбоев.** Исправлены несколько сбоев из-за нехватки памяти (при активном просмотре, загрузке обложек и интенсивной сетевой активности) — стабильнее на любых устройствах.
- **Плавнее интерфейс воспроизведения.** Ползунок больше не «зависает», а при возобновлении книги корректно восстанавливается выбранная скорость воспроизведения.
- **Поиск внутри источника теперь листает все результаты** в каждом каталоге — вы больше не ограничены первой страницей.
- **Надёжнее воспроизведение YouTube** — с автоматическим восстановлением и небольшой перемоткой назад, когда сессии нужно обновиться.
- **Счётчики просмотров стали компактными** (например, 15.9k вместо 15 937).
- **Дружелюбнее, переписанная справка** на всех 12 языках, а также доработанные тёмная и сумеречная темы.
- **Приложение открывает вашу первую онлайн-библиотеку при запуске**, а описание и отзывы к книге теперь загружаются сразу при открытии из поиска.

### Изменения поведения

- Нажатие «Назад» следует вашему реальному пути по приложению (в обратном хронологическом порядке), а не фиксированному порядку экранов.
- Карточки жанров/авторов/чтецов в глобальном поиске только открывают списки книг — они никогда не запускают воспроизведение.
- Свайп вправо по карточке из «Избранного» теперь открывает экран книги.
- Поиск внутри источника подгружает результаты при прокрутке, а не останавливается на первой странице.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ

- Нет

### Риски / Что протестировать

- Глобальный поиск: карточки сущностей (жанр/автор/чтец), переход в список книг карточки, бесконечная прокрутка и «Назад» из результатов.
- Навигация «Назад» по цепочкам (Плеер → Книга → Поиск → Категория → Библиотека) и после переключения источников.
- Воспроизведение: восстановление скорости и позиции при возобновлении; ползунок продолжает двигаться; пропуск тишины и нормализация.
- Долгое нажатие на книги и на название/автора/жанр книги; отмена индикатора долгого нажатия при отпускании/двойном касании.
- Локальный фильтр в «Истории» и «Избранном»; свайп влево для удаления; свайп вправо по «Избранному» открывает книгу.
- Загрузки, офлайн-воспроизведение и пауза/возобновление/отмена загрузки.
- Стабильность при активном просмотре и загрузке множества обложек (без сбоев).
- Экран справки и отрисовка тём (тёмная/сумеречная) на разных языках.
