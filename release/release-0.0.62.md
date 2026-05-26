# Release notes — 0.0.62

Release date: 26-May-2026

## English
- Resume after force-stop now restores the correct book and position. When the system kills the app (task-swipe-away, OEM cleanup, OS kill), the last-played book, track and playhead are recovered on next launch instead of jumping back to a stale or zero position.
- The previously-selected source is remembered across force-stops, so reopening the app no longer drops you on a default catalog after the OS task-kills the app.
- Sleep timer fade-out behavior is more reliable: the timer correctly recognizes when playback has reached the end and resets state instead of leaving the timer in an inconsistent ticking state.
- Pull-to-refresh on the book screen no longer gets stuck in a spinning "refreshing" state when the catalog fetch hangs — a watchdog now clears the indicator.
- Fixed a crash when opening the player screen during fast back-navigation.
- Restored playback for one of the streaming catalogs that recently broke due to an upstream anti-bot change; audio now resolves through a different mobile client path.
- Faster catalog scrolling and search: heavy regular-expression compilation in catalog parsing is now cached and reused.
- Smoother long downloads: large file and HLS downloads handle empty/partial responses more cleanly and surface a clearer error instead of failing late.
- Release builds now ship with logging fully disabled for slightly lower background overhead and zero log writes to disk.

### Behavior changes
- After an OS task-kill, the app resumes the last book at the last saved position; previously it could revert to an earlier position or restart the book.
- Tapping play after an end-of-track sleep-timer event leaves the timer cleanly cleared instead of carrying over residual state.
- Selecting "start over" (position 0) within a few minutes of a force-stop is honored as intentional and is not overridden by the recovery fallback.

### BREAKING CHANGES
- None

### Risks / What to test
- Open a book, play for ~1 minute, swipe the app away from recents, relaunch — confirm correct book, track and position are restored.
- Force-stop the app from system settings while a non-default source is selected; reopen and confirm that source is still active.
- Start a sleep timer with fade-out, let it reach the end of a track — verify the timer state resets and a new playback session starts clean.
- Pull-to-refresh on a slow or failing book screen; confirm the spinner clears within a few seconds even if data doesn't arrive.
- Navigate rapidly into and out of the player screen — verify no crash on opening the player.
- Verify playback works on the streaming catalog that previously failed with empty responses.
- Download a large track and an HLS stream; confirm progress and final file are correct, and errors are clear if interrupted.

## Русский
# Примечания к выпуску — 0.0.62

Дата выпуска: 26-May-2026

## Русский
- Возобновление воспроизведения после принудительной остановки теперь корректно восстанавливает книгу и позицию. Если систему «убила» приложение (свайп из «Недавних», очистка прошивкой производителя, kill от ОС), при следующем запуске возвращаются последняя книга, дорожка и точка воспроизведения — без отката на устаревшую или нулевую позицию.
- Ранее выбранный источник сохраняется после принудительной остановки приложения, и при повторном открытии вы не попадаете в каталог по умолчанию.
- Поведение таймера сна с плавным затуханием стало надёжнее: таймер корректно распознаёт окончание воспроизведения и сбрасывает состояние, не оставаясь в «висящем» режиме.
- Жест «потянуть для обновления» на экране книги больше не зависает в крутящемся состоянии при подвисшем запросе — сторожевой таймер очищает индикатор.
- Исправлен сбой при открытии экрана плеера во время быстрых переходов «назад».
- Восстановлено воспроизведение для одного из потоковых каталогов, недавно сломавшегося из-за изменений на стороне сервера; аудио теперь успешно получается через другой мобильный клиентский путь.
- Более быстрая прокрутка каталога и поиск: тяжёлая компиляция регулярных выражений при разборе каталога теперь кэшируется и переиспользуется.
- Большие загрузки стали стабильнее: загрузка больших файлов и HLS корректно обрабатывает пустые/частичные ответы и выдаёт понятную ошибку вместо позднего сбоя.
- Релизные сборки больше не пишут логи: чуть меньшая фоновая нагрузка и ноль записей на диск.

### Изменения поведения
- После kill от ОС приложение возобновляет последнюю книгу с последней сохранённой позиции; раньше оно могло откатиться на более раннюю точку или начать книгу заново.
- После события «конец дорожки» от таймера сна состояние таймера сбрасывается чисто и не переносится в следующую сессию.
- Выбор «начать сначала» (позиция 0) в течение нескольких минут после принудительной остановки трактуется как намеренное действие и не перезаписывается механизмом восстановления.

### BREAKING CHANGES
- Нет

### Риски / Что протестировать
- Откройте книгу, послушайте ~1 минуту, смахните приложение из «Недавних», перезапустите — убедитесь, что восстановлены правильная книга, дорожка и позиция.
- Принудительно остановите приложение через настройки системы при выбранном не-стандартном источнике; откройте приложение и убедитесь, что источник остался прежним.
- Запустите таймер сна с плавным затуханием и дождитесь окончания дорожки — проверьте, что состояние таймера сброшено и новая сессия воспроизведения начинается «с чистого листа».
- Используйте «потянуть для обновления» на медленном или сбойном экране книги; убедитесь, что индикатор исчезает за несколько секунд даже если данные не пришли.
- Быстро открывайте и закрывайте экран плеера — убедитесь, что нет сбоя при открытии.
- Проверьте, что воспроизведение работает на потоковом каталоге, ранее возвращавшем пустые ответы.
- Скачайте большой трек и HLS-поток; убедитесь, что прогресс и итоговый файл корректны, а при прерывании ошибка понятна.
