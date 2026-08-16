# Release notes — 0.0.81

Release date: 16-Aug-2026

## English
- **New: Library Backup & Restore.** Export your whole library — sources, favorites, listening history, bookmarks, ignore lists, and settings — into a single portable file, and restore it on the same device or a new one. The file is a standard `.json.gz` you can also open on a PC.
- Restore now brings back your listening history and works even into a completely fresh or empty library.
- **New: manage your source tabs.** Hide, reorder, and rename tabs, with your arrangement and visibility reliably remembered. Sources added in an app update now appear automatically without a reinstall.
- **New: ignore by title** (with `*` wildcard support), alongside ignoring by author or narrator, shown with clearer, unified strike-through icons.
- Unplayable titles are now clearly marked as **Locked** instead of silently vanishing from lists, and playable paid previews are no longer dropped.
- The lock-screen / notification no longer shows an empty placeholder tile when there is nothing to resume, and the collapsed notification keeps the correct title instead of the app name.
- More reliable resume after a long pause — playback re-prepares cleanly instead of getting stuck.
- Android Auto keeps the session alive while it stays connected, fixing dropped connections during browsing.
- The library top bar now shows the current folder after you change the local storage location.
- Fixed empty author / narrator listings on one online source after the site changed its layout.
- Smoother "load more" pagination and source switching — no stray extra loads or stalls.
- Proxy settings now take effect immediately after import or restore, without needing an app restart.
- **TV / D-pad remotes:** fixed Back behavior (no dead or "zombie" Back, no ghost Settings screen), a reliable focus highlight per tab, reaching the top bar from the first row, and moving through source chips and the Description / Reviews tabs.

### Behavior changes
- Source configuration moved to a single ordered list; on upgrade your existing order and visibility are migrated automatically, and newly shipped sources are added at the end (hidden or shown per their default).
- Backup files are sealed and validated on restore: corrupt, truncated, or non-STPlayer files are rejected. Backups made by older versions still restore.
- Backups no longer include transient interface state such as scroll position and search history.

### BREAKING CHANGES
- None. Older backups still restore and existing source settings migrate automatically.

### Risks / What to test
- Export, then restore on a clean install: verify sources, tab order, visibility, favorites, history, bookmarks, and ignore lists all return.
- Restore a backup made by a pre-0.0.81 build (legacy format).
- Reorder, hide, and rename source tabs; restart and confirm they persist; confirm a newly added source appears after an update.
- Ignore by title with a `*` wildcard; check strike-through rendering.
- Resume after a long pause; confirm the lock-screen tile is absent when there is nothing to resume.
- Android Auto: connect, browse, and play.
- TV remote: Back across screens, focus highlight, top-bar and chip navigation.
- Set a proxy via restore and confirm it applies without a restart.

## Русский
- **Новое: резервное копирование и восстановление библиотеки.** Экспортируйте всю библиотеку — источники, избранное, историю прослушивания, закладки, списки игнорирования и настройки — в один переносимый файл и восстанавливайте его на этом же или на новом устройстве. Файл — стандартный `.json.gz`, который можно открыть и на ПК.
- Восстановление теперь возвращает историю прослушивания и работает даже в полностью пустую библиотеку.
- **Новое: управление вкладками источников.** Скрывайте, меняйте порядок и переименовывайте вкладки — расположение и видимость надёжно запоминаются. Источники, добавленные в обновлении приложения, теперь появляются автоматически, без переустановки.
- **Новое: игнорирование по названию** (с поддержкой символа `*`), в дополнение к игнорированию по автору или чтецу; показывается едиными, более понятными значками с зачёркиванием.
- Недоступные для воспроизведения книги теперь явно помечаются как **Заблокировано** вместо того, чтобы молча исчезать из списков, а воспроизводимые платные превью больше не пропадают.
- Экран блокировки / уведомление больше не показывает пустую заглушку, когда нечего возобновлять, а свёрнутое уведомление сохраняет правильный заголовок вместо названия приложения.
- Более надёжное возобновление после долгой паузы — воспроизведение корректно переинициализируется, а не «зависает».
- Android Auto сохраняет сессию активной, пока подключён, устраняя обрывы соединения во время просмотра.
- Верхняя панель библиотеки теперь показывает текущую папку после смены места локального хранения.
- Исправлены пустые списки авторов / чтецов на одном онлайн-источнике после изменения вёрстки сайта.
- Более плавная подгрузка «ещё» и переключение источников — без лишних загрузок и зависаний.
- Настройки прокси теперь применяются сразу после импорта или восстановления, без перезапуска приложения.
- **ТВ / пульт (D-pad):** исправлено поведение кнопки «Назад» (нет «мёртвой» или «зомби»-кнопки, нет фантомного экрана настроек), надёжная подсветка фокуса на каждой вкладке, переход к верхней панели из первого ряда, а также перемещение по чипам источников и вкладкам «Описание / Отзывы».

### Изменения поведения
- Конфигурация источников переведена на единый упорядоченный список; при обновлении ваш текущий порядок и видимость мигрируют автоматически, а новые источники добавляются в конец (скрытыми или видимыми по умолчанию).
- Файлы резервных копий скрепляются печатью и проверяются при восстановлении: повреждённые, обрезанные или чужие файлы отклоняются. Копии, созданные старыми версиями, по-прежнему восстанавливаются.
- Резервные копии больше не включают временное состояние интерфейса, такое как позиция прокрутки и история поиска.

### BREAKING CHANGES
- Нет. Старые резервные копии по-прежнему восстанавливаются, а существующие настройки источников мигрируют автоматически.

### Риски / Что протестировать
- Экспорт, затем восстановление на чистой установке: проверить возврат источников, порядка вкладок, видимости, избранного, истории, закладок и списков игнорирования.
- Восстановление резервной копии, созданной сборкой до 0.0.81 (устаревший формат).
- Изменение порядка, скрытие и переименование вкладок источников; перезапуск и проверка сохранения; проверка появления нового источника после обновления.
- Игнорирование по названию с символом `*`; проверка отображения зачёркивания.
- Возобновление после долгой паузы; проверить отсутствие плитки на экране блокировки, когда нечего возобновлять.
- Android Auto: подключение, просмотр и воспроизведение.
- Пульт ТВ: «Назад» на разных экранах, подсветка фокуса, навигация по верхней панели и чипам.
- Задать прокси через восстановление и убедиться, что он применяется без перезапуска.
