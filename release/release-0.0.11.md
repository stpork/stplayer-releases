# Release notes — 0.0.11

Release date: 11-Feb-2026 

## English
- Improved metadata and progress loading across Library, History, and Favorites, especially for books opened from device storage and SAF folders.
- Better restoration of book details (cover/description/position) after reopening items from recent/favorite lists.
- Improved list layout when player controls are visible: bottom items are less likely to be hidden behind the mini-player.
- Better bottom navigation spacing on gesture-navigation devices, reducing awkward extra padding at the bottom.
- Improved playback-state handling around system audio focus changes for more reliable save/restore behavior.
- The app no longer grabs audio focus on startup, so it won’t interrupt music or podcasts already playing in other apps.
- Audio focus handling is now tied more closely to actual playback state, improving reliability when starting, pausing, and stopping.
- Library, History, and Favorites screens now keep extra space at the bottom when player controls are visible, so the last items are easier to see and interact with.
- Bottom player bar visuals were refined to better match system surfaces for a cleaner, more consistent look.

### Behavior changes
- When player controls are expanded, Library/History/Favorites now reserve extra bottom space so the last card remains accessible.
- Metadata/position lookup is now handled consistently across web, local-folder, and SAF-based books.
- Audio focus is now requested when playback listeners are registered for active playback, not during app initialization.
- Scrollable lists reserve additional bottom space while expanded player controls are shown.

### BREAKING CHANGES
- None

### Risks / What to test
- Open books from History/Favorites (web, local folder, SAF) and verify title/cover/progress restore correctly.
- With mini-player visible, scroll to the last item in Library/History/Favorites and confirm it is fully tappable.
- Test on gesture-navigation and 3-button navigation devices for bottom bar spacing.
- Pause/resume with interruptions (phone call, other audio app) and verify progress is saved.
- Start the app while another audio app is playing; verify playback is not interrupted.
- Start playback in this app; verify audio focus is acquired correctly.
- Pause/stop playback and switch apps; verify focus is released as expected.
- In Library, History, and Favorites, confirm bottom items remain accessible when player controls are visible.

## Русский
- Улучшена загрузка метаданных и прогресса в разделах Библиотека, История и Избранное, особенно для книг из локального хранилища и SAF-папок.
- Улучшено восстановление данных книги (обложка/описание/позиция) при повторном открытии из недавних и избранных.
- Улучшена верстка списков при видимых элементах управления плеером: нижние элементы теперь реже перекрываются мини-плеером.
- Улучшены отступы нижней навигации на устройствах с жестовой навигацией, стало меньше лишнего пустого пространства снизу.
- Улучшена обработка состояния воспроизведения при изменениях аудиофокуса системы для более надежного сохранения/восстановления позиции.
- Приложение больше не запрашивает аудиофокус при запуске, поэтому не прерывает музыку или подкасты, которые уже воспроизводятся в других приложениях.
- Обработка аудиофокуса теперь точнее привязана к фактическому состоянию воспроизведения, что повышает надежность при старте, паузе и остановке.
- На экранах Библиотеки, Истории и Избранного добавлен дополнительный отступ снизу при видимых элементах управления плеером, поэтому последние элементы списка лучше видны и удобнее для нажатия.
- Внешний вид нижней панели плеера доработан: она лучше сочетается с системными поверхностями и выглядит более цельно.

### Behavior changes
- Когда элементы управления плеером развернуты, в Библиотеке/Истории/Избранном теперь резервируется дополнительное пространство снизу, чтобы последняя карточка оставалась доступной.
- Поиск метаданных и позиции теперь работает единообразно для веб-книг, локальных папок и книг из SAF.
- Аудиофокус теперь запрашивается при регистрации слушателей для активного воспроизведения, а не во время инициализации приложения.
- Прокручиваемые списки резервируют дополнительное место снизу, когда показаны развернутые элементы управления плеером.

### BREAKING CHANGES
- None

### Risks / What to test
- Откройте книги из Истории/Избранного (веб, локальная папка, SAF) и проверьте корректное восстановление названия/обложки/прогресса.
- При видимом мини-плеере прокрутите до последнего элемента в Библиотеке/Истории/Избранном и убедитесь, что его можно полностью нажать.
- Проверьте отступы нижней панели на устройствах с жестовой и кнопочной навигацией.
- Проверьте паузу/возобновление при прерываниях (звонок, другое аудио-приложение) и сохранение позиции.
- Запустите приложение, пока в другом приложении уже играет аудио; убедитесь, что воспроизведение не прерывается.
- Запустите воспроизведение в этом приложении; убедитесь, что аудиофокус запрашивается корректно.
- Поставьте на паузу/остановите воспроизведение и переключайтесь между приложениями; убедитесь, что аудиофокус освобождается как ожидается.
- В Библиотеке, Истории и Избранном проверьте, что нижние элементы списка остаются доступными при видимых контролах плеера.
