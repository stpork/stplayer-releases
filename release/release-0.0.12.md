# Release notes — 0.0.12

Release date: 11-Feb-2026 

## English
- Fixed playback position saving so manual seek, track selection, and book switches are stored immediately, reducing incorrect resume points.
- Improved reliability of progress/history updates by preventing delayed older save events from overwriting newer playback state.
- Updated bottom navigation/player layout handling to reduce unnecessary empty space on screens with gesture navigation.
- Refined list screen spacing (Library, Favorites, History) so content uses visible space more consistently near the bottom.
- Improved search UX in Library: exiting search is now available directly from the top bar with a clearer active-search state.
- Refreshed player bottom bar visual styling with a smoother gradient for better readability and cleaner transitions.
- Reduced live progress refresh frequency when appropriate, improving UI efficiency and lowering background churn.

### Behavior changes
- Exiting Library search is now done from the top app bar search control.
- Playback position after seek/track change/book switch is persisted immediately.
- Bottom spacing behavior on list screens is tighter and less padded.

### BREAKING CHANGES
- None

### Risks / What to test
- Seek in a track, close/reopen, and confirm resume starts at the new position.
- Switch tracks/books quickly and verify progress/history remains correct.
- Test Library search enter/exit flow and query reset behavior.
- Check Library/Favorites/History bottom spacing on gesture and 3-button navigation modes.
- Verify mini-player/bottom bar visuals and controls readability across themes.

## Русский
- Исправлено сохранение позиции воспроизведения: при перемотке, выборе трека и переключении книги позиция теперь сохраняется сразу, что уменьшает случаи неверного продолжения.
- Повышена надежность обновления прогресса и истории: отложенные старые события сохранения больше не перезаписывают более новое состояние воспроизведения.
- Улучшена работа нижних отступов и области плеера: на устройствах с жестовой навигацией стало меньше лишнего пустого пространства.
- Скорректированы отступы в списках (Библиотека, Избранное, История), чтобы контент стабильнее использовал видимую область у нижнего края.
- Улучшен UX поиска в Библиотеке: выход из поиска теперь доступен прямо в верхней панели, с более понятной индикацией активного поиска.
- Обновлен визуальный стиль нижней панели плеера: градиент стал более плавным для лучшей читаемости и более аккуратных переходов.
- Снижена частота обновления живого прогресса в подходящих сценариях, что повышает эффективность UI и уменьшает фоновую нагрузку.

### Behavior changes
- Выход из поиска в Библиотеке теперь выполняется через элемент поиска в верхней панели.
- Позиция воспроизведения после перемотки/смены трека/переключения книги сохраняется сразу.
- Поведение нижних отступов в экранах списков стало более компактным, с меньшим количеством лишнего пространства.

### BREAKING CHANGES
- None

### Risks / What to test
- Выполнить перемотку внутри трека, закрыть/открыть приложение и проверить, что воспроизведение продолжается с новой позиции.
- Быстро переключать треки/книги и убедиться, что прогресс и история сохраняются корректно.
- Проверить сценарии входа/выхода из поиска в Библиотеке и сброс поискового запроса.
- Проверить нижние отступы в Библиотеке/Избранном/Истории на жестовой и 3-кнопочной навигации.
- Проверить визуал мини-плеера/нижней панели и читаемость элементов управления в разных темах.