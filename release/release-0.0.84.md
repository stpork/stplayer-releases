I have enough to write user-facing notes. The 20 commits reduce to a handful of user-visible fixes; the rest are refactors/tests (excluded).

# Release notes — 0.0.84

Release date: 21-Aug-2026

## English
- Fixed the play/pause button on car controls, headsets, and TV remotes not resuming a book after the app was relaunched — a single press now correctly picks up where you left off.
- Play from a car's steering-wheel or dashboard controls now works even when automatic resume is turned off, as long as a book is already open.
- Fixed pagination when browsing large audiobook categories: pages no longer overlap or repeat items after using search.
- Fixed a rare case where reopening certain multi-track books restored the wrong position and skipped the first track; playback now starts correctly.
- Removed "ghost audio": if playback times out with a network error, audio can no longer unexpectedly resume in the background while the error screen is showing.
- Restored richer folder/book browsing details (track formats, listening progress) that were missing in some listings.
- TV: fixed keyboard/remote focus jumping behind dialogs when changing playback speed, pitch, sleep timer, bookmarks, or picking a file.
- TV: smoother and more consistent left/right navigation across all Library grids, and focus now returns to the card you came from when pressing Back in Favorites and History.

### Behavior changes
- On cold start, a single external play/pause (headset, car, TV remote) now resumes the last book instead of doing nothing.
- Car media controls are treated as a real user action, so they can start playback even with automatic resume disabled.

### BREAKING CHANGES
- None

### Risks / What to test
- Resume from headset, car controls, and TV remote after fully closing and reopening the app.
- Browse deep into large audiobook categories after running a search — check pages don't overlap or repeat.
- Reopen older multi-track books and confirm they start at the right place.
- Trigger a network stall/error and confirm audio does not resume behind the error screen.
- On TV: open speed, pitch, sleep-timer, bookmark, and file dialogs; confirm focus stays on the dialog and returns correctly after Back in Favorites/History.

## Русский
- Исправлена кнопка воспроизведения/паузы на автомобильных пультах, гарнитурах и пультах ТВ, которая не возобновляла книгу после перезапуска приложения — теперь одно нажатие корректно продолжает с места остановки.
- Запуск с рулевых или приборных кнопок в автомобиле теперь работает даже при отключённом автоматическом возобновлении, если книга уже открыта.
- Исправлена постраничная навигация при просмотре больших категорий аудиокниг: страницы больше не перекрываются и не повторяют элементы после использования поиска.
- Исправлен редкий случай, когда при повторном открытии некоторых многодорожечных книг восстанавливалась неверная позиция и пропускалась первая дорожка; воспроизведение теперь запускается корректно.
- Убрано «фантомное аудио»: если воспроизведение прерывается по тайм-ауту из-за сетевой ошибки, звук больше не может неожиданно возобновиться в фоне, пока показан экран ошибки.
- Восстановлены расширенные сведения при просмотре папок и книг (форматы дорожек, прогресс прослушивания), которых не хватало в некоторых списках.
- ТВ: исправлен увод фокуса пульта за диалоги при изменении скорости, тона, таймера сна, закладок и при выборе файла.
- ТВ: более плавная и единообразная навигация влево/вправо по всем сеткам библиотеки, а фокус теперь возвращается на исходную карточку при нажатии «Назад» в Избранном и Истории.

### Изменения поведения
- При холодном запуске одно внешнее нажатие воспроизведения/паузы (гарнитура, автомобиль, пульт ТВ) теперь возобновляет последнюю книгу, а не игнорируется.
- Автомобильные медиа-кнопки воспринимаются как реальное действие пользователя, поэтому могут запускать воспроизведение даже при отключённом автоматическом возобновлении.

### BREAKING CHANGES
- Нет

### Риски / Что протестировать
- Возобновление с гарнитуры, автомобильных кнопок и пульта ТВ после полного закрытия и повторного открытия приложения.
- Просмотр вглубь больших категорий аудиокниг после выполнения поиска — проверить, что страницы не перекрываются и не повторяются.
- Повторное открытие старых многодорожечных книг и проверка запуска с правильной позиции.
- Спровоцировать сетевой сбой/ошибку и убедиться, что звук не возобновляется за экраном ошибки.
- На ТВ: открыть диалоги скорости, тона, таймера сна, закладок и выбора файла; убедиться, что фокус остаётся на диалоге и корректно возвращается после «Назад» в Избранном и Истории.
