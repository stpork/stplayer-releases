# Release notes — 0.0.69

Release date: 03-Jul-2026

## English
- Fixed a bug where a book that was paused before force-closing the app would silently resume playing on the next launch instead of staying paused.
- Fixed playback history and per-book resume sometimes restoring an incorrect or unbounded playback speed.
- Fixed a mismatch that could resolve the wrong audio source when resuming a book from History or Android Auto.
- Improved source matching so books are correctly matched by their library name, not just an internal identifier — reduces "wrong source" issues after resuming from History.
- Various stability fixes around speed and pitch handling to keep playback settings consistent across restarts.

### Behavior changes
- Cold-start restore after force-killing the app now always resumes in a paused state, matching what was saved — no more surprise autoplay.
- Playback speed values are now consistently kept within the supported 0.5×–2.0× range when restoring saved sessions, history, or downloads.

### BREAKING CHANGES
None

### Risks / What to test
- Force-kill the app while a book is playing, then paused; relaunch and confirm it stays paused in both cases.
- Resume a book from History and from Android Auto for sources where the display name differs from the internal source ID; confirm it plays from the correct source.
- Check playback speed/pitch persist correctly across app restarts, including books with previously saved out-of-range speed values.
- Verify downloaded and SAF-based books restore position and speed correctly.

## Русский

Дата релиза: 03-Jul-2026

- Исправлена ошибка, из-за которой книга, поставленная на паузу перед принудительным закрытием приложения, при следующем запуске могла тихо начать воспроизводиться сама — вместо того чтобы остаться на паузе.
- Исправлены случаи, когда история воспроизведения и возобновление конкретной книги восстанавливали некорректную или неограниченную скорость воспроизведения.
- Исправлено несоответствие, из-за которого при возобновлении книги из Истории или Android Auto мог выбираться не тот источник аудио.
- Улучшено сопоставление источников: книги теперь корректно сопоставляются по отображаемому имени в библиотеке, а не только по внутреннему идентификатору — это уменьшает случаи "не того источника" после возобновления из Истории.
- Различные исправления стабильности в обработке скорости и высоты тона, обеспечивающие сохранность настроек воспроизведения при перезапусках.

### Изменения поведения
- Восстановление после холодного старта (после принудительного закрытия приложения) теперь всегда возобновляется в состоянии паузы, соответствующем сохранённому — больше никакого неожиданного автовоспроизведения.
- Значения скорости воспроизведения теперь стабильно удерживаются в поддерживаемом диапазоне 0.5×–2.0× при восстановлении сохранённых сессий, истории или загрузок.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
Отсутствуют

### Риски / Что проверить
- Принудительно закрыть приложение во время воспроизведения книги, а также во время паузы; перезапустить и убедиться, что состояние паузы сохраняется в обоих случаях.
- Возобновить воспроизведение книги из Истории и из Android Auto для источников, у которых отображаемое имя отличается от внутреннего ID источника; убедиться, что воспроизведение идёт из правильного источника.
- Проверить, что скорость и высота тона воспроизведения корректно сохраняются при перезапусках приложения, включая книги с ранее сохранёнными значениями скорости вне допустимого диапазона.
- Убедиться, что загруженные книги и книги через SAF корректно восстанавливают позицию и скорость воспроизведения.
