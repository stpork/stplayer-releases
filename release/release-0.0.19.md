# Release notes — 0.0.19

Release date: 15-Feb-2026 

## English
- Added a full bookmark manager in Player: create bookmarks with custom time/title/icon, edit existing bookmarks, delete them, and jump directly to saved points.
- Improved bookmark controls: the bookmark button now reflects whether a book already has bookmarks, so saved marks are easier to spot at a glance.
- Fixed cases where adding a favorite could fail or appear to disappear for items not yet fully present in history (including local and web sources).
- Improved favorites category reliability: existing category favorites are preserved and automatically migrated to the new unified storage format.
- Fixed resume-position behavior after deleting an item from History: reopening that item now starts from the beginning instead of an old saved position.
- Improved context menu clarity for local items by hiding download actions when they are not applicable.
- Improved interaction feedback in Mini Player with haptic response during horizontal swipe gestures.
- Improved list resilience: some remote library views now auto-refresh when returning to an empty list, reducing “empty until manual refresh” cases.

### Behavior changes
- Bookmarking is now dialog-based with add/edit/delete and quick jump from the same screen.
- Deleting an item from History also clears its saved resume point.
- Local-only entries no longer show download actions unless download is actually applicable.

### BREAKING CHANGES
- None

### Risks / What to test
- Create/edit/delete bookmarks and verify jump-to-bookmark accuracy.
- Toggle favorites on new/local/web items and confirm they persist after app restart.
- Delete a history item, reopen it, and verify playback starts at 0:00.
- Open context menus for local vs remote items and verify download actions appear only when relevant.

## Русский
- Добавлен полноценный менеджер закладок в плеере: можно создавать закладки с настраиваемыми временем/названием/иконкой, редактировать их, удалять и быстро переходить к нужному месту.
- Улучшены элементы управления закладками: кнопка закладки теперь показывает, есть ли у книги сохранённые закладки, поэтому их легче заметить сразу.
- Исправлены случаи, когда добавление в избранное могло не сработать или «исчезать» для элементов, которые ещё не полностью появились в истории (включая локальные и веб-источники).
- Повышена надёжность категорий избранного: существующие избранные категории сохраняются и автоматически переносятся в новый единый формат хранения.
- Исправлено поведение позиции продолжения после удаления из истории: при повторном открытии воспроизведение теперь начинается с начала, а не со старой сохранённой позиции.
- Улучшена ясность контекстного меню для локальных элементов: действия загрузки скрываются, если они неприменимы.
- Улучшена обратная связь в мини-плеере: добавлен тактильный отклик при горизонтальном свайпе.
- Повышена устойчивость списков: некоторые удалённые разделы библиотеки теперь автоматически обновляются при возврате на пустой список, уменьшая случаи «пусто до ручного обновления».

### Behavior changes
- Работа с закладками теперь происходит через диалог: добавление, редактирование, удаление и быстрый переход из одного экрана.
- Удаление элемента из истории теперь также сбрасывает сохранённую позицию продолжения.
- Для локальных элементов действия загрузки больше не показываются, если загрузка фактически неприменима.

### BREAKING CHANGES
- None

### Risks / What to test
- Создание/редактирование/удаление закладок и точность перехода по закладке.
- Переключение избранного для новых/локальных/веб-элементов и проверка сохранения после перезапуска приложения.
- Удаление элемента из истории, повторное открытие и проверка старта воспроизведения с 0:00.
- Проверка контекстного меню для локальных и удалённых элементов: действия загрузки должны отображаться только когда это уместно.