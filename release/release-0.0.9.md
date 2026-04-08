# Release notes — 0.0.9

Release date: 10-Feb-2026 

## English
- Library search is now faster to reuse: recent queries are saved, suggested as you type, and can be removed individually.
- Search input behavior is cleaner: extra spaces are trimmed automatically before search runs.
- Search mode got new controls for showing/hiding the keyboard and a clearer one-tap exit action.
- Fixed an issue where loading a later page could disrupt browsing: already loaded items now stay visible if page 2+ fails.
- Improved pagination stability by stopping repeated auto-retries after persistent errors on later pages.
- Improved playback position reliability when switching books, so resume data is saved for the correct previous item and track.
- Improved layout on devices with gesture/navigation bars so the mini player and controls are less likely to overlap system UI.
- Fixed search routing for Poleknig so queries open the expected search results page directly.

### Behavior changes
- Search history is now persisted and shown as suggestions during typing.
- Very short queries are ignored until they are long enough to be meaningful.
- If a later pagination page fails, the app keeps existing results and stops auto-loading more pages.
- Book-switch position saves now keep the previous book’s playlist context for more accurate resume.

### BREAKING CHANGES
- None

### Risks / What to test
- Run several searches, verify suggestions appear, can be tapped, and can be removed.
- Confirm short queries do not trigger remote search unexpectedly.
- Scroll through paginated lists and simulate page-2+ failures; verify loaded items remain visible.
- Switch between books/tracks and verify resume returns to the correct track and timestamp.
- Check mini player and bottom controls on devices with gesture and 3-button navigation.

## Русский
- Поиск в библиотеке стал удобнее для повторного использования: последние запросы сохраняются, подсказываются при вводе и могут удаляться по одному.
- Поведение строки поиска стало чище: лишние пробелы автоматически убираются перед запуском поиска.
- В режиме поиска добавлены новые элементы управления для показа/скрытия клавиатуры и более понятный выход в одно нажатие.
- Исправлена проблема при загрузке следующих страниц: если страница 2+ не открылась, уже загруженные элементы остаются на экране.
- Улучшена стабильность пагинации: при постоянной ошибке на следующих страницах прекращаются бесконечные автоповторы.
- Повышена надежность сохранения позиции при переключении книг: прогресс теперь сохраняется для правильного предыдущего трека и книги.
- Улучшена верстка на устройствах с жестовой/системной навигацией, чтобы мини-плеер и контролы меньше перекрывались системным интерфейсом.
- Исправлена маршрутизация поиска для Poleknig: запросы теперь сразу открывают корректную страницу результатов.

### Behavior changes
- История поиска теперь сохраняется и показывается как подсказки во время ввода.
- Слишком короткие запросы игнорируются, пока не достигнут полезной длины.
- Если следующая страница пагинации не загружается, приложение сохраняет уже полученные результаты и прекращает авто-загрузку новых страниц.
- При переключении книг сохранение позиции теперь фиксирует контекст предыдущего плейлиста для более точного возобновления.

### BREAKING CHANGES
- None

### Risks / What to test
- Выполнить несколько поисков, проверить появление подсказок, выбор по нажатию и удаление отдельных записей.
- Убедиться, что слишком короткие запросы не запускают удаленный поиск.
- Прокрутить списки с пагинацией и смоделировать ошибку на странице 2+; проверить, что уже загруженные элементы остаются.
- Переключаться между книгами/треками и проверить, что возобновление идет с правильного трека и времени.
- Проверить мини-плеер и нижние контролы на устройствах с жестовой и кнопочной навигацией.