# Release notes — 0.0.92

Release date: 03-Oct-2026

## English

- Earlier books stay available when you scroll back through large catalogues.
- Additional online book details are saved for later visits and preserved as more pages load.
- Reopening the app preserves your selected catalogue.
- Empty History and Favorites tabs no longer leave the startup screen waiting.
- Favorites handle rapid repeated taps correctly and report save failures.
- Known book titles remain visible in History and Favorites when the library folder is temporarily unavailable.
- Fixed progress displays freezing in books with multiple chapters and unknown total duration.
- The player layout stays steady while loading, and the mini player stops showing a loading indicator after a playback error.
- Playback errors, source menus and generated chapter labels now follow your selected app language.
- Android Auto and Bluetooth show consistent playback symbols, and book covers continue to display after app restarts.
- Fixed torrent playback retry handling when audio is missing or playback is cancelled.

### Behavior changes

- While waiting for audio, the progress bar turns grey and the play button shows a spinner instead of a loading message.
- If a favorite change cannot be saved, the star returns to its previous state and an error message appears.
- Starting playback from another source switches the library to that source. Restoring the last played book preserves your saved catalogue selection.
- Playback can begin while additional book details are still loading.

### BREAKING CHANGES

None

### Risks / What to test

- Browse several catalogue pages, scroll back and open earlier books.
- Restart the app and check catalogue selection, saved book details and playback position.
- Add and remove favorites rapidly; check persistence after restart and feedback when saving fails.
- Temporarily revoke library-folder access and check that known titles remain visible.
- Check buffering, seeking and chapter transitions, including books with unknown total duration and stalled torrent audio.
- Change the app language; check labels, errors, playback symbols and covers in Android Auto and Bluetooth.

## Русский

- Ранее загруженные книги остаются доступны при прокрутке больших каталогов назад.
- Дополнительные сведения об онлайн-книгах сохраняются для следующих посещений и не теряются при загрузке новых страниц.
- При повторном открытии приложения сохраняется выбранный каталог.
- Пустые вкладки «История» и «Избранное» больше не задерживают закрытие стартового экрана.
- Быстрые повторные нажатия на звёздочку обрабатываются корректно; при ошибке сохранения появляется сообщение.
- Известные названия книг остаются видимыми в «Истории» и «Избранном», даже если папка библиотеки временно недоступна.
- Исправлено зависание отображения прогресса в книгах с несколькими главами и неизвестной общей длительностью.
- Элементы плеера не смещаются во время загрузки, а мини-плеер перестаёт показывать индикатор загрузки после ошибки воспроизведения.
- Сообщения об ошибках воспроизведения, меню источников и автоматически созданные подписи глав теперь используют выбранный язык приложения.
- В Android Auto и Bluetooth используются единообразные значки состояния воспроизведения, а обложки продолжают отображаться после перезапуска приложения.
- Исправлена обработка повторных попыток при отсутствии аудиоданных торрента и отмене воспроизведения.

### Изменения в поведении

- При ожидании аудио полоса прогресса становится серой, а кнопка воспроизведения показывает индикатор загрузки вместо текстового сообщения.
- Если изменение в «Избранном» не удалось сохранить, звёздочка возвращается в прежнее состояние и появляется сообщение об ошибке.
- Запуск воспроизведения из другого источника переключает библиотеку на этот источник. Восстановление последней прослушанной книги сохраняет выбранный каталог.
- Воспроизведение может начаться, пока дополнительные сведения о книге ещё загружаются.

### НЕСОВМЕСТИМЫЕ ИЗМЕНЕНИЯ

Нет

### Риски / Что проверить

- Просмотрите несколько страниц каталога, прокрутите назад и откройте ранее загруженные книги.
- Перезапустите приложение и проверьте выбранный каталог, сохранённые сведения о книгах и позицию воспроизведения.
- Быстро добавляйте и удаляйте книги из «Избранного»; проверьте результат после перезапуска и сообщение при ошибке сохранения.
- Временно отзовите доступ к папке библиотеки и убедитесь, что известные названия книг остаются видимыми.
- Проверьте ожидание аудио, перемотку и переходы между главами, включая книги с неизвестной общей длительностью и торренты без поступающих аудиоданных.
- Смените язык приложения; проверьте подписи, сообщения об ошибках, значки воспроизведения и обложки в Android Auto и Bluetooth.