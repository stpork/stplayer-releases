# Release notes — 0.0.16

Release date: 13-Feb-2026 

## English
- Added haptic feedback for long-press actions in the book/player screen, making hold gestures feel clearer.
- Improved playback position saving reliability to reduce incorrect resume points after quick state changes.
- Improved stability of library pagination after memory pressure, so lists recover cleanly and continue loading.
- Updated sleep timer motion-reset defaults for better out-of-the-box behavior on new setups.
- Refined Settings labels and icons (including localized text) for faster scanning and easier navigation.

### Behavior changes
- Non-periodic playback-position saves are now debounced by 1 second, with the latest action taking priority.
- App exit/task removal/destroy flows now save playback position immediately.
- Sleep timer motion reset now defaults to `Always`, with default sensitivity adjusted to 47%.

### BREAKING CHANGES
- None

### Risks / What to test
- Pause/seek/rewind, close the app, reopen, and verify resume position accuracy.
- Switch between books quickly and confirm each book restores the correct position.
- Start/cancel sleep timer and confirm position persistence remains correct.
- Verify long-press haptics on cover artwork and long-press actions.
- Check updated Settings labels/icons in your language.

## Русский
- Добавлена тактильная отдача для действий по долгому нажатию на экране книги/плеера, чтобы удержание ощущалось понятнее.
- Повышена надежность сохранения позиции воспроизведения, чтобы уменьшить случаи неверного продолжения после быстрых смен состояния.
- Улучшена стабильность пагинации в библиотеке после нехватки памяти: списки корректно восстанавливаются и продолжают подгрузку.
- Обновлены значения по умолчанию для сброса таймера сна по движению для более удобного поведения «из коробки» при новых настройках.
- Обновлены подписи и иконки в «Настройках» (включая локализованный текст) для более быстрого ориентирования.

### Изменения поведения
- Непериодические сохранения позиции воспроизведения теперь выполняются с debounce 1 секунда, приоритет у последнего действия.
- При выходе из приложения/удалении задачи/уничтожении сервиса позиция воспроизведения теперь сохраняется сразу.
- Сброс таймера сна по движению теперь по умолчанию `Always`, чувствительность по умолчанию изменена на 47%.

### BREAKING CHANGES
- None

### Риски / Что протестировать
- Пауза/перемотка назад/вперед, закрытие приложения, повторный запуск: проверить точность продолжения.
- Быстрое переключение между книгами: убедиться, что для каждой восстанавливается правильная позиция.
- Запуск/отмена таймера сна: проверить корректность сохранения позиции.
- Проверить тактильный отклик при долгом нажатии на обложку и другие long-press действия.
- Проверить обновленные подписи/иконки в «Настройках» на вашем языке.