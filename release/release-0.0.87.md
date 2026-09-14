# Release notes — 0.0.87

Release date: 15-Sep-2026

## English

- Improved listening-position saving, including for downloaded books.
- Changing playback speed now preserves your latest saved listening position.
- Cancelling the sleep timer stops the volume fade and restores the volume.
- Improved Android TV search navigation, including when no results are found.

### Behavior changes

- On Android TV, use Left/Right to select search, clear and keyboard buttons. Press OK in the search field to open the keyboard; directional navigation resumes after you close it.
- Cancelling a sleep timer during a fade immediately restores the volume.

### BREAKING CHANGES

None

### Risks / What to test

- Check that online and downloaded books resume at the correct position after pausing, switching books and restarting the app.
- Change playback speed, including back to normal, and check that both speed and position are retained.
- Cancel the sleep timer while the volume is fading.
- On Android TV, search, clear the query and close the keyboard with and without results.

## Русский

- Повышена надёжность сохранения позиции прослушивания, в том числе для скачанных книг.
- Изменение скорости воспроизведения теперь сохраняет последнюю сохранённую позицию прослушивания.
- Отмена таймера сна останавливает затухание звука и восстанавливает громкость.
- Улучшена навигация по поиску на Android TV, в том числе при отсутствии результатов.

### Изменения в поведении

- На Android TV стрелками влево/вправо можно выбрать кнопки поиска, очистки и клавиатуры. Нажатие OK в поле поиска открывает клавиатуру; после её закрытия снова доступна навигация стрелками.
- Отмена таймера сна во время затухания сразу восстанавливает громкость.

### НЕСОВМЕСТИМЫЕ ИЗМЕНЕНИЯ

Нет

### Риски / Что проверить

- Проверьте восстановление позиции в онлайн- и скачанных книгах после паузы, переключения между книгами и перезапуска приложения.
- Измените скорость воспроизведения, в том числе верните обычную, и проверьте сохранение скорости и позиции.
- Отмените таймер сна во время затухания звука.
- На Android TV проверьте поиск, очистку запроса и закрытие клавиатуры при наличии и отсутствии результатов.