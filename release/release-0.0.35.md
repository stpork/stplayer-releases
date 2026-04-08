# Release notes — 0.0.35

Release date: 20-Mar-2026 

## English
- Added built-in support for three more online audiobook sources: Patephone, LibriVox, and Digitalbook.io.
- Patephone now offers richer discovery with genres, collections, recommendations, and separate search for books, authors, and narrators.
- Long online catalog lists now load more reliably, including when the first page fits on screen or when you reach the bottom while scrolling.
- The Player screen can now show embedded cover art from MP3, M4A, and M4B files, and it updates when the track changes.
- Fixed Patephone playback so books resolve fresh playable stream links more reliably.
- Fixed book info menus showing wrong author or narrator details for some items.
- Digitalbook.io browsing and playback are more stable, with better metadata handling and more reliable external audio links.

### Behavior changes
- If Resume playback mode is set to Last played audiobook, the app now opens directly to the Player screen on launch when a last played book exists.
- When you reset the sleep timer by shaking the phone during fade-out, the volume is restored first, and the fade time is added after the timer instead of being counted inside it.

### BREAKING CHANGES
None

### Risks / What to test
- Browse and play books from Patephone, including genres, collections, authors, and narrators.
- Browse and play books from LibriVox and Digitalbook.io.
- Verify long lists keep loading when you scroll and when the first page does not fill the screen.
- Check that embedded cover art appears on the Player screen and updates on track changes.
- Test startup with Resume playback mode set to Last played audiobook, and test sleep timer reset during fade-out.

## Русский
- Добавлена встроенная поддержка ещё трёх онлайн-источников аудиокниг: Патефон, LibriVox и Digitalbook.io.
- В Патефоне стало удобнее искать книги: появились жанры, подборки, рекомендации и отдельный поиск по книгам, авторам и чтецам.
- Длинные онлайн-каталоги теперь подгружаются надёжнее, в том числе когда первая страница целиком помещается на экран или когда вы доходите до конца списка при прокрутке.
- Экран плеера теперь показывает встроенные обложки из файлов MP3, M4A и M4B, и обложка обновляется при смене трека.
- Исправлено воспроизведение из Патефона: книги теперь надёжнее получают актуальные ссылки для запуска.
- Исправлены случаи, когда в меню информации о книге показывался неверный автор или чтец.
- Просмотр и воспроизведение книг из Digitalbook.io стали стабильнее: улучшена работа с метаданными и внешними аудиоссылками.

### Изменения поведения
- Если для режима возобновления выбрано Last played audiobook, приложение теперь сразу открывает экран плеера при запуске, если последняя книга существует.
- Если сбросить таймер сна встряхиванием телефона во время затухания, громкость сначала восстанавливается, а время затухания теперь добавляется после таймера, а не входит в его длительность.

### Критические изменения
Отсутствуют

### Риски / Что проверить
- Открытие и воспроизведение книг из Патефона, включая жанры, подборки, авторов и чтецов.
- Открытие и воспроизведение книг из LibriVox и Digitalbook.io.
- Проверить, что длинные списки продолжают подгружаться при прокрутке и когда первая страница не заполняет экран.
- Проверить, что встроенные обложки появляются на экране плеера и обновляются при смене трека.
- Проверить запуск приложения с режимом Resume playback = Last played audiobook, а также сброс таймера сна во время затухания.