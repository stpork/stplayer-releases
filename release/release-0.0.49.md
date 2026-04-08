# Release notes — 0.0.49

Release date: 08-Apr-2026 

## English
- Pull-to-refresh on supported web book pages and source lists now forces a live reload instead of reusing stale cached pages.
- Book descriptions are more reliable: full verified descriptions are kept after refresh and reopen, while empty results no longer bring back old teaser snippets.
- Cover art is more stable across the library, book screen, mini player, and player screen, with fewer unexpected cover swaps and better fallback to saved covers when live artwork is missing.
- The mini-player loading spinner now appears only during real startup or buffering and no longer stays over the artwork once playback is already running.
- Loyal Books browsing has been expanded with a new Languages section, localized language names, and clearer category navigation.
- Visible library items now pick up metadata sooner, and loading more results after a refresh is more reliable.
- Saved torrent and downloaded items keep synced metadata and cover art more reliably when reopened.
- Several source fixes improved missing metadata, covers, categories, and playable links for AKG, Loyal Books, PLK, PTP, RTR, SHK, and BYT.

### Behavior changes
- Refreshing a supported web book or source list now bypasses cached HTML and fetches fresh data.
- Loyal Books category browsing now includes Languages alongside the main category tabs when available.
- The mini-player spinner hides once playback is already progressing.

### BREAKING CHANGES
- None

### Risks / What to test
- Refresh a web book page and confirm updated description, cover, or track info appears immediately.
- Browse Loyal Books categories, especially Languages, and open a language-specific catalog.
- Start playback from the library and verify the mini-player spinner and cover art behavior.
- Reopen saved torrent or downloaded items and confirm metadata and artwork are preserved.
- Spot-check affected sources: AKG, Loyal Books, PLK, PTP, RTR, SHK, and BYT.

## Русский
- Обновление свайпом на поддерживаемых страницах веб-книг и в списках источников теперь принудительно загружает свежие данные вместо повторного использования устаревшего кэша.
- Описания книг стали надежнее: полные проверенные описания сохраняются после обновления и повторного открытия, а пустой результат больше не подменяется старым коротким фрагментом.
- Работа с обложками стала стабильнее в библиотеке, на странице книги, в мини-плеере и в плеере: стало меньше неожиданных подмен обложки, а сохраненные обложки надежнее используются как запасной вариант, если онлайн-обложка недоступна.
- Индикатор загрузки в мини-плеере теперь показывается только при реальном запуске или буферизации и не остается поверх обложки, когда воспроизведение уже идет.
- В Loyal Books расширена навигация: добавлен раздел «Языки», локализованные названия языков и более понятная навигация по категориям.
- Видимые элементы библиотеки теперь получают метаданные раньше, а подгрузка следующих результатов после обновления работает надежнее.
- Сохраненные torrent- и downloaded-элементы теперь надежнее сохраняют синхронизированные метаданные и обложки при повторном открытии.
- Исправления нескольких источников улучшили недостающие метаданные, обложки, категории и воспроизводимые ссылки для AKG, Loyal Books, PLK, PTP, RTR, SHK и BYT.

### Изменения в поведении
- Обновление поддерживаемой веб-книги или списка источника теперь обходит HTML-кэш и загружает свежие данные.
- В навигации Loyal Books теперь может отображаться раздел «Языки» рядом с основными вкладками категорий.
- Индикатор загрузки в мини-плеере скрывается, как только воспроизведение действительно продолжается.

### Ломающие изменения
- Нет

### Риски / Что проверить
- Обновите страницу веб-книги и убедитесь, что описание, обложка или список треков сразу подтягиваются в свежем виде.
- Проверьте категории Loyal Books, особенно раздел «Языки», и откройте каталог по конкретному языку.
- Запустите воспроизведение из библиотеки и проверьте поведение индикатора загрузки мини-плеера и обложки.
- Повторно откройте сохраненные torrent- или downloaded-элементы и убедитесь, что метаданные и обложки сохранены.
- Точечно проверьте затронутые источники: AKG, Loyal Books, PLK, PTP, RTR, SHK и BYT.