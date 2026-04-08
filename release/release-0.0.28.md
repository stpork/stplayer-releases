# Release notes — 0.0.28

Release date: 01-Mar-2026 

## English
- Added "Recent" section to the library browser — quickly access your recently played audiobooks from the main navigation.
- Improved background playback reliability — media session now continues running when the app is backgrounded on Android 12+ devices, ensuring uninterrupted playback.
- Fixed empty library state — app no longer crashes when the library contains no playable content.
- Optimized book screen performance — reduced UI recompositions when navigating to individual books for smoother experience.
- Improved download progress accuracy — better progress estimation for long audiobooks with many tracks.

### Behavior changes
- "Recent" category now appears in the library root when browsing via Android Auto, Bluetooth, or other media browsers.
- When foreground service cannot start due to Android 12+ background restrictions, playback continues in background mode instead of stopping.

### BREAKING CHANGES
None

### Risks / What to test
- Verify playback continues when app is backgrounded on Android 12+ devices
- Confirm "Recent" section appears and shows correct items in the library browser
- Test library with no content to ensure empty state is handled gracefully

## Русский
- Добавлен раздел "Недавние" в браузере библиотеки — быстрый доступ к недавно прослушанным аудиокнигам из главной навигации.
- Улучшена надёжность воспроизведения в фоновом режиме — медиасессия продолжает работать при переводе приложения в фон на устройствах с Android 12+, обеспечивая бесперебойное воспроизведение.
- Исправлена ошибка с пустой библиотекой — приложение больше не вылетает, когда библиотека не содержит воспроизводимого контента.
- Оптимизирована производительность экрана книги — уменьшено количество перекомпоновок UI при переходе к отдельным книгам для более плавной работы.
- Улучшена точность индикации загрузки — более точная оценка прогресса для длинных аудиокниг с большим количеством треков.

### Изменения в поведении
- Категория "Недавние" теперь отображается в корне библиотеки при просмотре через Android Auto, Bluetooth или другие медиабраузеры.
- Когда невозможно запустить foreground-сервис из-за ограничений Android 12+, воспроизведение продолжается в фоновом режиме вместо остановки.

### Критические изменения
Отсутствуют

### Риски / Что проверить
- Убедитесь, что воспроизведение продолжается при переводе приложения в фон на устройствах с Android 12+
- Подтвердите, что раздел "Недавние" отображается и показывает правильные элементы в браузере библиотеки
- Проверьте работу библиотеки без контента, чтобы убедиться в корректной обработке пустого состояния
