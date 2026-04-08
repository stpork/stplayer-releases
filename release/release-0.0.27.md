# Release notes — 0.0.27

Release date: 01-Mar-2026 

## English
- Books marked as completed (green checkmark) now persist across app restarts. The completion state is only cleared when you explicitly replay the book from the beginning.
- Improved Android Auto and Bluetooth metadata display — book titles and part numbers now show correctly on car dashboards and paired devices.
- Added full media key support on Android TV — stop, next track, previous track, fast forward, and rewind buttons now work correctly.
- Optimized seeking for different stream types — local files use precise seeking while streams use closest-sync for smoother navigation.
- Improved library screen responsiveness — metadata updates now load progressively in batches for smoother scrolling.
- Fixed TV home screen layout and focus handling.

### Behavior changes
- None

### BREAKING CHANGES
- None

### Risks / What to test
- Verify book completion state persists after killing and relaunching the app
- Test Android Auto/Bluetooth metadata display with multi-part audiobooks
- Test media keys on Android TV remote

## Русский
- Книги, отмеченные как завершённые (зелёная галочка), теперь сохраняются после закрытия и повторного запуска приложения. Состояние завершения сбрасывается только при явном повторном воспроизведении книги с начала.
- Улучшено отображение метаданных в Android Auto и Bluetooth — названия книг и номера частей теперь корректно отображаются на автомобильных панелях и подключённых устройствах.
- Добавлена полная поддержка медиаклавиш на Android TV — кнопки стоп, следующий трек, предыдущий трек, перемотка вперёд и назад теперь работают корректно.
- Оптимизировано перемещение по аудио для разных типов потоков — локальные файлы используют точную перемотку, а потоки используют ближайшую синхронизацию для более плавной навигации.
- Улучшена отзывчивость экрана библиотеки — обновления метаданных теперь загружаются постепенно пакетами для более плавной прокрутки.
- Исправлена компоновка и обработка фокуса на главном экране ТВ.

### Изменения поведения
- Отсутствуют

### Критические изменения
- Отсутствуют

### Риски / Что проверить
- Проверьте, что состояние завершения книги сохраняется после закрытия и повторного запуска приложения
- Протестируйте отображение метаданных Android Auto/Bluetooth для многочастных аудиокниг
- Проверьте работу медиаклавиш на пульте Android TV
