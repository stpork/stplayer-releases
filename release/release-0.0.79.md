I have the commit list, stats, and file breakdown — the truncated remainder is diff content (AGENTS.md prose), which won't add user-facing value beyond what the commits already tell me. I have enough to write user-facing notes.

Consolidating the ~280 commits: the bulk is Android TV D-pad/focus + Back-button work, a large audit-driven stability/data-integrity/performance pass, refresh-button UX, source management, and dependency bumps (which I'll exclude unless there's user impact — Media3 playback lib bump is borderline but internal).

# Release notes — 0.0.79

Release date: 11-Aug-2026

## English

- **Android TV / Fire TV is now fully usable with the D-pad.** You can open and operate the side menu, move between the top bar, source tabs, category chips, search field and the content grid, and navigate every screen without a mouse.
- **Reliable Back button on TV.** A single Back press no longer unexpectedly quits the app; Back now returns you to the right place (grid, book, or the exact card you came from) and opens the menu where expected.
- **Full player controls on TV.** The progress bar is now the focus target with visible focus highlighting, and remote transport keys (play/pause, next/previous, channel up/down) map to seeking and page-jumps.
- **Book screen on TV** supports D-pad throughout — focus the cover to open the player, long-press OK for the context menu, and the description scrolls properly at its end.
- **Refresh button** added to the top bar on the Library and Book screens (phone and TV), showing the standard pull-to-refresh spinner on phone. The stuck refresh indicator on TV is fixed.
- **New source management screen** to organize and rename your audiobook sources.
- **Playback stability improvements**: smoother recovery from network stalls, more reliable resume after long pauses, and fewer stuck or duplicated playback states.
- **Fewer lost positions and safer data**: playback position, history, favorites, and downloads are saved more durably, with better protection against corruption during writes and interrupted operations.
- **Downloads** keep partial data when a torrent download is cancelled instead of discarding it, and correctly reuse the same network settings as playback.
- **Category titles** in the top bar now use the full available width while keeping action icons visible.
- **Performance and battery**: smoother scrolling and progress updates, lower memory use when the app is in the background, and reduced background work while paused or idle.
- **Layout and appearance polish** across the library, favorites, history, and player screens, plus refreshed on-device Help for TV D-pad controls in all supported languages.

### Behavior changes

- On TV, a single Back press never exits the app; use it to step back through screens or close the menu.
- On TV, the mini-player progress bar is no longer focusable (it was never seekable there).
- The refresh action now appears as a top-bar icon rather than only pull-to-refresh.

### BREAKING CHANGES

- None

### Risks / What to test

- TV/Fire TV: menu open/close, moving between top bar / tabs / chips / grid, Back behavior from Player, Book and Search, and player transport via the remote.
- Phone: top-bar refresh and pull-to-refresh, category title layout with action icons.
- Playback: resume after a long pause, recovery after a network stall, position saved correctly after switching books.
- Downloads: cancel a torrent download and confirm partial data is kept.
- Data: favorites, history, and source selection persist across app restarts.

## Русский

- **Android TV / Fire TV теперь полностью управляется пультом (D-pad).** Можно открывать и использовать боковое меню, переходить между верхней панелью, вкладками источников, чипами категорий, полем поиска и сеткой контента, перемещаться по всем экранам без мыши.
- **Надёжная кнопка «Назад» на ТВ.** Одно нажатие «Назад» больше не закрывает приложение неожиданно; «Назад» возвращает в нужное место (сетка, книга или именно та карточка, откуда вы пришли) и открывает меню там, где это ожидается.
- **Полное управление плеером на ТВ.** Полоса прогресса теперь является объектом фокуса с видимой подсветкой, а кнопки пульта (play/pause, вперёд/назад, каналы вверх/вниз) отвечают за перемотку и переход по страницам.
- **Экран книги на ТВ** полностью работает с D-pad — сфокусируйтесь на обложке, чтобы открыть плеер, долгое нажатие OK вызывает контекстное меню, а описание корректно прокручивается до конца.
- **Кнопка обновления** добавлена в верхнюю панель на экранах Библиотеки и Книги (телефон и ТВ) со стандартным индикатором обновления на телефоне. Исправлен зависавший индикатор обновления на ТВ.
- **Новый экран управления источниками** для организации и переименования ваших источников аудиокниг.
- **Улучшения стабильности воспроизведения**: более плавное восстановление после сетевых сбоев, надёжное возобновление после долгих пауз, меньше зависших или дублирующихся состояний воспроизведения.
- **Меньше потерь позиции и сохраннее данные**: позиция воспроизведения, история, избранное и загрузки сохраняются надёжнее, с лучшей защитой от повреждения при записи и прерванных операциях.
- **Загрузки** сохраняют частичные данные при отмене торрент-загрузки вместо их удаления и корректно используют те же сетевые настройки, что и воспроизведение.
- **Заголовки категорий** в верхней панели теперь используют всю доступную ширину, сохраняя видимость значков действий.
- **Производительность и батарея**: более плавная прокрутка и обновление прогресса, меньше расхода памяти в фоне, меньше фоновой работы во время паузы или простоя.
- **Косметические улучшения оформления и вёрстки** на экранах библиотеки, избранного, истории и плеера, а также обновлённая встроенная Справка по управлению D-pad на ТВ на всех поддерживаемых языках.

### Behavior changes

- На ТВ одно нажатие «Назад» никогда не закрывает приложение; используйте его для перехода назад по экранам или закрытия меню.
- На ТВ полоса прогресса мини-плеера больше не фокусируется (перемотка там всё равно не работала).
- Действие обновления теперь отображается значком в верхней панели, а не только через жест «потянуть для обновления».

### BREAKING CHANGES

- Нет

### Risks / What to test

- ТВ/Fire TV: открытие/закрытие меню, переходы между верхней панелью / вкладками / чипами / сеткой, поведение «Назад» из плеера, книги и поиска, управление плеером с пульта.
- Телефон: обновление из верхней панели и жестом, вёрстка заголовка категории со значками действий.
- Воспроизведение: возобновление после долгой паузы, восстановление после сетевого сбоя, корректное сохранение позиции после смены книги.
- Загрузки: отмена торрент-загрузки с сохранением частичных данных.
- Данные: сохранение избранного, истории и выбранного источника после перезапуска приложения.
