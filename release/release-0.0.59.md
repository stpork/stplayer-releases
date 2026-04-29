# Release notes — 0.0.59

Release date: 29-Apr-2026

## English
- New **Reviews** tab on the book page: read user reviews and comments from supported sources, with replies, ratings, and links back to the original page.
- New **Description / Reviews** tabs layout — full description always visible, with reviews available for sources that provide them.
- Aggregate ratings shown inline next to the description on sources that expose only a single rating value.
- Book descriptions are now cleaner and more complete: fixed cases where descriptions appeared truncated (showing only the first ~300 characters) or had ragged blank-line gaps.
- The link to the original book page now appears above the tabs for easier access.
- Pull-to-refresh added on Book, Library, and Player screens.
- Search-off icon is tinted red while a search filter is active, making the active state easier to spot.
- Reordered source priority so faster, more reliable sources are tried first when finding a book.
- Smoother scrolling and faster source switching, especially on lower-end devices.
- Reduced memory footprint when browsing many books across multiple sources.
- Fixed several production crashes reported from real users, including a crash that occurred when the previously chosen download folder had been deleted outside the app.
- Fixed cases where the description was missing or partial on certain sources.
- Cleaner notification and analytics behavior — no more performance/analytics telemetry collected; only crash reporting remains.

### Behavior changes
- The book page now uses tabs (Description / Reviews) instead of a single description block. Sources without reviews still show only the description.
- When the saved download folder is no longer accessible, the app will ask you to pick the folder again on the next download instead of failing silently.
- If multiple devices are connected, the developer test runner now requires choosing one explicitly (developer-facing only).

### BREAKING CHANGES
- None

### Risks / What to test
- Open books from each source and confirm the description shows in full and the Reviews tab loads (where supported).
- Verify replies render correctly and ratings/votes are shown where the source provides them.
- Test pull-to-refresh on Book, Library, and Player screens.
- Toggle search and confirm the active icon turns red.
- Browse many books in a row and confirm the app stays responsive and doesn't grow in memory unexpectedly.
- Try a download after deleting the previously chosen download folder from a file manager — the app should ask you to re-pick the folder, not crash.
- Confirm playback, downloads, and library merging still work normally.

## Русский
- Новая вкладка **Отзывы** на странице книги: читайте отзывы и комментарии пользователей с поддерживаемых источников, с ответами, оценками и ссылками на оригинальную страницу.
- Новая раскладка вкладок **Описание / Отзывы** — полное описание всегда на виду, отзывы доступны для источников, которые их предоставляют.
- Сводный рейтинг показывается рядом с описанием для источников, у которых есть только одно значение рейтинга.
- Описания книг теперь чище и полнее: исправлены случаи, когда описание выглядело обрезанным (только первые ~300 символов) или содержало рваные пустые строки.
- Ссылка на оригинальную страницу книги теперь расположена над вкладками — её удобнее найти.
- Добавлен жест «потяни, чтобы обновить» на экранах Книги, Библиотеки и Плеера.
- Иконка отключения поиска подсвечивается красным, когда фильтр поиска активен — активное состояние стало заметнее.
- Изменён порядок источников: более быстрые и надёжные источники теперь пробуются первыми при поиске книги.
- Более плавная прокрутка и быстрое переключение между источниками, особенно на менее мощных устройствах.
- Снижено потребление памяти при просмотре большого количества книг из разных источников.
- Исправлены несколько падений в продакшене, о которых сообщили реальные пользователи, в том числе падение, возникавшее при удалении ранее выбранной папки загрузок вне приложения.
- Исправлены случаи отсутствия или неполного описания для некоторых источников.
- Более чистая телеметрия — больше не собираются данные аналитики и производительности, осталась только отправка отчётов о падениях.

### Изменения в поведении
- Страница книги теперь использует вкладки (Описание / Отзывы) вместо одного блока описания. У источников без отзывов по-прежнему отображается только описание.
- Если сохранённая папка загрузок больше недоступна, приложение попросит выбрать её заново при следующей загрузке вместо тихой ошибки.
- При подключении нескольких устройств тестовый запуск теперь требует явного выбора одного (касается только разработчиков).

### BREAKING CHANGES
- Нет

### Риски / Что проверить
- Открыть книги из каждого источника и убедиться, что описание отображается полностью, а вкладка «Отзывы» загружается (где поддерживается).
- Проверить, что ответы отображаются корректно, а оценки/голоса показываются там, где источник их предоставляет.
- Проверить «потяни, чтобы обновить» на экранах Книги, Библиотеки и Плеера.
- Включить поиск и убедиться, что активная иконка становится красной.
- Просмотреть подряд много книг и убедиться, что приложение остаётся отзывчивым и не растёт по памяти.
- Попробовать загрузку после удаления ранее выбранной папки загрузок через файловый менеджер — приложение должно попросить выбрать папку заново, а не упасть.
- Убедиться, что воспроизведение, загрузки и объединение библиотеки работают как раньше.
