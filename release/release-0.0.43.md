# Release notes — 0.0.43

Release date: 01-Apr-2026 

## English
- Improved resume reliability for Android Auto, Bluetooth/headset controls, and media buttons when STPlayer starts from the background or after the app was closed.
- The app now restores the correct book, queue, chapter, and position more reliably for local, downloaded, and web content, even if track links or playlist order changed.
- Fixed stale or invalid saved sessions causing broken resumes; STPlayer now rebuilds resume data automatically when possible.
- Leaving the app now clears external auto-resume data, reducing unexpected restarts from car or headset controls.
- Web audiobook playback preferences such as skip silence and loudness normalization now persist more reliably between sessions.
- Improved startup stability on newer Android versions, reducing missed play commands and failed launches from external controls.

### Behavior changes
- Android Auto can resume your last session even when `Headset/Bluetooth only` is enabled and no headset is currently connected.
- If `Resume playback` is set to `Never`, external resume requests no longer reopen the last session.
- If a saved queue no longer matches the available tracks, STPlayer restores more safely and avoids auto-starting the wrong item.
- Exiting the app clears saved external resume state, so old sessions should not come back through car or headset controls.

### BREAKING CHANGES
- None

### Risks / What to test
- Resume playback from Android Auto after force-closing the app.
- Test Bluetooth/headset buttons and media buttons from a cold start, especially on Android 12+.
- Verify that `Never` and `Headset/Bluetooth only` behave as expected.
- Check that local, downloaded, and web books resume on the correct chapter and position.
- Exit the app and confirm old sessions do not restart unexpectedly from external controls.

## Русский
- Улучшена надежность возобновления через Android Auto, Bluetooth/гарнитурные кнопки и медиа-кнопки, когда STPlayer запускается из фона или после полного закрытия приложения.
- Приложение теперь надежнее восстанавливает правильную книгу, очередь, главу и позицию для локального, загруженного и веб-контента, даже если ссылки на треки или порядок плейлиста изменились.
- Исправлены случаи, когда устаревшие или поврежденные сохраненные сессии ломали возобновление; теперь STPlayer по возможности автоматически пересобирает данные для продолжения.
- При выходе из приложения теперь очищаются данные внешнего автопродолжения, поэтому автомобильные системы и гарнитуры реже запускают старое воспроизведение неожиданно.
- Настройки воспроизведения для веб-аудиокниг, такие как пропуск тишины и нормализация громкости, теперь надежнее сохраняются между сессиями.
- Улучшена стабильность запуска на новых версиях Android: внешние команды воспроизведения теперь реже теряются, а запуск из внешних контроллеров реже завершается неудачей.

### Изменения поведения
- Android Auto теперь может возобновлять последнюю сессию даже если включен режим `Headset/Bluetooth only` и гарнитура в данный момент не подключена.
- Если параметр `Resume playback` установлен в `Never`, внешние запросы на продолжение больше не открывают последнюю сессию.
- Если сохраненная очередь больше не совпадает с доступными треками, STPlayer восстанавливает состояние безопаснее и не запускает автоматически неправильный элемент.
- При выходе из приложения сохраненное состояние внешнего возобновления очищается, поэтому старые сессии не должны возвращаться через автомобильные или гарнитурные кнопки.

### Несовместимые изменения
- Нет

### Риски / Что проверить
- Проверьте возобновление через Android Auto после принудительного закрытия приложения.
- Проверьте Bluetooth/гарнитурные кнопки и медиа-кнопки при холодном старте, особенно на Android 12 и новее.
- Убедитесь, что режимы `Never` и `Headset/Bluetooth only` работают ожидаемо.
- Проверьте, что локальные, загруженные и веб-книги продолжаются с правильной главы и позиции.
- Выйдите из приложения и убедитесь, что старые сессии не запускаются неожиданно через внешние контроллеры.