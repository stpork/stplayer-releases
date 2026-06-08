# Release notes — 0.0.65

Release date: 08-Jun-2026

## English

- **Favorites protected from data loss** — a race condition that could silently wipe your favorites list during app startup or background refresh has been fixed; favorites are no longer overwritten by an empty in-memory state before the library finishes loading from disk.
- **Broken catalog sections hidden automatically** — the app now quietly checks whether each category tab (e.g. Authors, Series, Genres) is still reachable on the server; tabs that return an error or have been removed are hidden rather than shown as empty or broken. Pull-to-refresh re-checks and can restore them if the server recovers.
- **Pull-to-refresh actually fetches fresh content** — a caching bug caused pull-to-refresh to return the same stale page within the cache window; it now correctly bypasses the cache and fetches from the server.
- **Local audiobook names parsed correctly** — folder names following the "Author – Title (Performer)" convention are now split properly: the performer is shown in the correct field instead of being merged into the title, and titles no longer include the author prefix.
- **"Home" sort option added to the sort menu** — sources that offer a default/homepage sort now expose it as a dedicated "Home" tab in the sort dropdown alongside New and Popular.
- **Localization improved across 12 languages** — over 300 native-fluency edits to German, Spanish, Finnish, French, Japanese, Dutch, Portuguese, Russian, Swedish, Turkish, and Chinese strings; favorite/unfavorite actions use shorter, unambiguous labels in all locales.
- **One source now shows 3 sort tabs** (Home / New / Popular) and pagination works correctly after a recent site layout change.

### Behavior changes

- Category tabs that are no longer served by the source website will disappear from the tab bar; pulling down to refresh can bring them back if availability changes.
- Favorites that existed on disk are preserved even if the in-memory list is empty at the time of a sync — the app will never silently unfavorite books due to a startup race.
- The "Home" sort option, where available, is now the default sort instead of "New/Newest first".

### BREAKING CHANGES

None

### Risks / What to test

- Add a book to Favorites, kill the app immediately, reopen — confirm favorites are intact.
- Remove the last favorited book — confirm it is actually removed (not preserved by the new guard).
- Open a source with multiple category tabs; verify tabs load, broken ones are hidden, pull-to-refresh restores a previously hidden tab if its URL is healthy again.
- Pull-to-refresh on any source — confirm fresh content loads (not cached stale content).
- Open a local audiobook with a folder named "Author – Title (Performer)" — verify author, title, and performer fields are all populated correctly in the player.
- Check the sort dropdown on sources with a "Home" option — confirm it appears and selecting it loads the correct page.
- Verify favorites/unfavorite actions display correctly in all tested locales.

---

## Русский

# Заметки к выпуску — 0.0.65

Дата выпуска: 08-июн-2026

## Русский

- **Избранное защищено от потери данных** — исправлена гонка, при которой список избранного мог молча затираться в момент запуска приложения или фонового обновления; избранное больше не перезаписывается пустым состоянием в памяти, пока библиотека ещё не успела загрузиться с диска.
- **Недоступные разделы каталога скрываются автоматически** — приложение теперь тихо проверяет, доступна ли каждая вкладка категории (например, «Авторы», «Серии», «Жанры») на сервере; вкладки, которые возвращают ошибку или были удалены, скрываются вместо того, чтобы отображаться пустыми или сломанными. Обновление свайпом вниз повторяет проверку и может восстановить вкладку, если сервер снова стал доступен.
- **Обновление свайпом действительно загружает свежий контент** — ошибка кэширования приводила к тому, что свайп-обновление возвращало ту же устаревшую страницу в пределах окна кэша; теперь запрос корректно обходит кэш и обращается к серверу.
- **Имена локальных аудиокниг парсятся правильно** — папки, оформленные по схеме «Автор – Название (Чтец)», теперь корректно разбираются: чтец отображается в нужном поле, а не сливается с названием, и в название больше не попадает имя автора.
- **Добавлена сортировка «Главная» в меню сортировки** — источники, предлагающие сортировку по главной странице, теперь показывают её как отдельную вкладку «Главная» в выпадающем меню наряду с «Новые» и «Популярные».
- **Локализация улучшена для 12 языков** — более 300 правок на естественность перевода для немецкого, испанского, финского, французского, японского, нидерландского, португальского, русского, шведского, турецкого и китайского языков; действия «В избранное» / «Из избранного» теперь используют короткие, однозначные подписи во всех языках.
- **Один из источников теперь показывает 3 вкладки сортировки** (Главная / Новые / Популярные), а пагинация работает корректно после недавних изменений на сайте.

### Изменения в поведении

- Вкладки категорий, которые больше не обслуживаются сайтом-источником, исчезнут из панели вкладок; обновление свайпом вниз может вернуть их, если доступность изменится.
- Избранное, сохранённое на диске, теперь сохраняется даже если в памяти список пуст в момент синхронизации — приложение никогда не удалит книги из избранного из-за гонки при запуске.
- Сортировка «Главная», где доступна, теперь является сортировкой по умолчанию вместо «Новые/Сначала новые».

### Критические изменения

Отсутствуют

### Риски / Что тестировать

- Добавить книгу в избранное, сразу завершить приложение, открыть снова — убедиться, что избранное на месте.
- Удалить последнюю книгу из избранного — убедиться, что она действительно удалена (а не сохранена новым защитным механизмом).
- Открыть источник с несколькими вкладками категорий; убедиться, что вкладки загружаются, сломанные скрываются, а обновление свайпом восстанавливает ранее скрытую вкладку, если её URL снова доступен.
- Обновление свайпом на любом источнике — убедиться, что загружается свежий контент, а не кэшированный устаревший.
- Открыть локальную аудиокнигу с папкой вида «Автор – Название (Чтец)» — проверить, что поля автора, названия и чтеца заполнены корректно.
- Проверить меню сортировки на источниках с опцией «Главная» — убедиться, что она отображается и при выборе загружает правильную страницу.
- Убедиться, что действия «В избранное» / «Из избранного» корректно отображаются на всех проверяемых языках.
