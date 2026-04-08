# Release notes — 0.0.14

Release date: 12-Feb-2026 

## English
- Improved navigation flow between Library, Book, and Player screens with more predictable swipe and Back button behavior.
- Added mini-player gesture improvements: horizontal swipes now switch screens more reliably, and long-press opens the current book context actions.
- Book details screen now shows cleaner metadata interactions (author/performer/genre), including better handling of multiple values and category navigation.
- Duration display on book details is now more accurate, using detailed track data when available.
- Player progress now includes a live percentage indicator, making playback position easier to track at a glance.
- Cover art handling is more reliable: better source matching, improved high-resolution cover selection, and fewer incorrect/reused covers across different books.
- Scraping and metadata loading were optimized to prioritize user-triggered actions, improving responsiveness when opening books and loading details.
- Playback/background behavior is more stable with improved lifecycle handling and power usage control during idle/non-playing states.

### Behavior changes
- Opening the app with only a `book_id` no longer automatically navigates to the Player screen.
- Starting playback from Library/History/Favorites keeps you on the current screen instead of forcing a jump to Player.
- In category views, Android Back now consistently returns to the previous library context.

### BREAKING CHANGES
- None

### Risks / What to test
- Verify Back/swipe navigation across Library, Book, and Player in all directions.
- Start playback from Book, History, and Favorites and confirm expected screen stays active.
- Check several providers to confirm correct cover art and metadata (especially author/performer/genre links).
- Validate duration and progress percentage on short and long audiobooks.
- Test app background/foreground transitions during playback and pause.

## Русский
- Улучшена навигация между экранами Библиотеки, Книги и Плеера: свайпы и кнопка Back теперь работают более предсказуемо.
- Добавлены улучшения жестов мини-плеера: горизонтальные свайпы надежнее переключают экраны, а долгое нажатие открывает контекстные действия для текущей книги.
- Экран информации о книге получил более удобную работу с метаданными (автор/исполнитель/жанр), включая корректную обработку нескольких значений и переходы по категориям.
- Отображение длительности на экране книги стало точнее за счет использования подробных данных по трекам, когда они доступны.
- В прогрессе плеера теперь показывается текущий процент воспроизведения, что упрощает контроль позиции.
- Работа с обложками стала надежнее: улучшено сопоставление источников, выбор изображений более высокого качества и снижено число неправильных/повторяющихся обложек у разных книг.
- Оптимизирована загрузка скрейпинга и метаданных с приоритетом пользовательских действий, что повышает отзывчивость при открытии книг и деталей.
- Повышена стабильность воспроизведения и поведения в фоне за счет улучшенной обработки жизненного цикла и энергопотребления в неактивных состояниях.

### Behavior changes
- Открытие приложения только с `book_id` больше не переводит автоматически на экран Плеера.
- Запуск воспроизведения из Библиотеки/Истории/Избранного оставляет вас на текущем экране, без принудительного перехода в Плеер.
- В режиме категорий кнопка Back теперь стабильно возвращает в предыдущий контекст библиотеки.

### BREAKING CHANGES
- None

### Risks / What to test
- Проверьте навигацию Back/свайпами между Библиотекой, Книгой и Плеером во всех направлениях.
- Запустите воспроизведение из Книги, Истории и Избранного и убедитесь, что активным остается ожидаемый экран.
- Проверьте несколько источников на корректность обложек и метаданных (особенно ссылок автор/исполнитель/жанр).
- Проверьте длительность и процент прогресса на коротких и длинных аудиокнигах.
- Протестируйте переходы приложения в фон/из фона во время воспроизведения и паузы.