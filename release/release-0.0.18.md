# Release notes — 0.0.18

Release date: 14-Feb-2026 

## English
- Resume progress saving is now faster and more reliable during playback, especially for local files and SAF folders.
- Periodic progress updates now preserve existing metadata and bookmarks more safely.
- Playback service startup is more stable when Android temporarily blocks background starts, reducing repeated failed attempts.
- Mini player interactions feel better with optional haptic feedback on seek taps and long-press actions.
- Background sensor and storage work was reduced in frequent idle/periodic paths for better efficiency.

### Behavior changes
- Very small periodic position changes (under ~1.5 seconds) may be skipped to reduce unnecessary writes; important events still force an immediate durable save.
- After a denied background service start, automatic retries are delayed for about 60 seconds unless the app is in foreground.
- Mini player tap and long-press gestures now trigger haptics when haptics are enabled.

### BREAKING CHANGES
None

### Risks / What to test
- Play audio, pause, resume, and confirm resume position is correct after reopening.
- Verify lock screen/headset/Bluetooth controls when app is in background.
- Test SAF folder playback and confirm progress/bookmarks remain correct.
- Check mini player tap-to-seek and long-press behavior with haptics on/off.

## Русский
- Сохранение точки продолжения стало быстрее и надежнее во время воспроизведения, особенно для локальных файлов и SAF-папок.
- Периодические обновления прогресса теперь безопаснее сохраняют существующие метаданные и закладки.
- Запуск сервиса воспроизведения стал стабильнее в случаях, когда Android временно блокирует фоновый старт, что уменьшает повторные неудачные попытки.
- Взаимодействие с мини-плеером стало приятнее: добавлена опциональная тактильная отдача для тапа по прогрессу и долгого нажатия.
- В частых сценариях простоя и периодического сохранения снижена фоновая нагрузка сенсоров и хранилища для лучшей эффективности.

### Изменения в поведении
- Очень маленькие периодические изменения позиции (меньше ~1,5 секунды) могут пропускаться, чтобы уменьшить лишние записи; важные события по-прежнему принудительно сохраняются сразу и надежно.
- После отклоненного фонового старта сервиса автоматические повторы откладываются примерно на 60 секунд, если приложение не на переднем плане.
- Жесты тапа и долгого нажатия в мини-плеере теперь дают тактильный отклик, если он включен.

### ЛОМАЮЩИЕ ИЗМЕНЕНИЯ
Нет

### Риски / Что протестировать
- Запустить воспроизведение, поставить на паузу, возобновить и проверить корректность позиции после повторного открытия.
- Проверить управление с экрана блокировки/гарнитуры/Bluetooth, когда приложение в фоне.
- Протестировать воспроизведение из SAF-папки и убедиться, что прогресс и закладки сохраняются корректно.
- Проверить работу мини-плеера (тап по прогрессу и долгое нажатие) при включенной и выключенной тактильной отдаче.