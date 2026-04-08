# Release notes — 0.0.15

Release date: 13-Feb-2026 

## English
- Improved torrent playback reliability, including safer fallback handling when opening torrent-based books.
- Better stability after memory pressure, with cleaner recovery of playback/scraper runtime components.
- Library and history cover images now render more smoothly, with faster placeholder display and more reliable fallback loading.
- Listening progress on library cards now refreshes more consistently after position saves.
- Noticeable battery and background-efficiency improvements during playback and metadata processing.
- Torrent cache handling is more robust, reducing stale cache entries and long-session slowdowns.

### Behavior changes
- Background metadata extraction now waits for charging and a non-low-battery state.
- On metered networks or Battery Saver mode, background detail fetching is more conservative to reduce battery/data usage.
- Playback position UI updates are slightly less frequent to improve battery efficiency.

### BREAKING CHANGES
- None

### Risks / What to test
- Start and seek within torrent playback, then resume after app restart.
- Verify library/history covers load correctly, including fallback images.
- Check that library listening progress updates after play/pause and after reopening the app.
- Confirm metadata extraction jobs run when device is charging and battery is not low.

## Русский
- Повышена надежность торрент-воспроизведения, включая более безопасный резервный путь при открытии книг из torrent-источников.
- Улучшена стабильность после нехватки памяти: компоненты воспроизведения и скрейпинга корректнее восстанавливаются.
- Обложки в библиотеке и истории отображаются плавнее: плейсхолдер появляется быстрее, а fallback-загрузка работает надежнее.
- Прогресс прослушивания в карточках библиотеки теперь обновляется стабильнее после сохранения позиции.
- Заметно улучшена энергоэффективность и фоновая работа во время воспроизведения и обработки метаданных.
- Обработка торрент-кеша стала устойчивее, что уменьшает накопление устаревших записей и замедления при долгой работе приложения.

### Behavior changes
- Фоновое извлечение метаданных теперь запускается только при зарядке и при не-низком уровне батареи.
- В режиме энергосбережения или в тарифицируемой сети фоновая загрузка деталей работает более бережно, чтобы снизить расход батареи и трафика.
- Обновление UI-позиции воспроизведения происходит немного реже для экономии заряда.

### BREAKING CHANGES
- None

### Risks / What to test
- Запустите торрент-воспроизведение, выполните перемотку и проверьте восстановление после перезапуска приложения.
- Проверьте загрузку обложек в библиотеке/истории, включая fallback-обложки.
- Убедитесь, что прогресс прослушивания в библиотеке обновляется после play/pause и после повторного открытия приложения.
- Подтвердите, что задачи извлечения метаданных выполняются при подключенной зарядке и нормальном уровне батареи.