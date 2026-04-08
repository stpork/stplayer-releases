# Release notes — 0.0.46

Release date: 04-Apr-2026

## English
- Android Auto now offers a cleaner browse experience with a single "Sources" entry that follows your library tab order, and source pages show filters like categories and sort options before the book list.
- Background playback is more reliable: repeated headset, Bluetooth, and media-button signals are less likely to cause duplicate starts or lost seek commands, and notification actions wake the player more consistently.
- Remote controllers and car kits (Android Auto) now show a custom button row with quick access to favorite toggle, playback speed, skip silence, loudness normalization, and sleep timer.
- Multi-chapter audiobooks now display a correct global timeline on Bluetooth devices, car systems, and Android Auto, with previous/next chapter buttons in the media button row.
- Cover art now appears more reliably for local folders, downloads, and private files across the library, history, notifications, and Android Auto.
- The app now awaits pending position saves before shutting down, so playback position is less likely to be lost on service stop.
- Saved books in history and favorites reconnect to their original source more reliably, improving artwork loading and reopen behavior.
- Protected links now fail cleanly with a wrong password instead of sometimes showing corrupted text.
- Downloaded books are recognized more reliably after refresh or restart, including relinked folders and partial downloads.

### Behavior changes
- The burst-protection window for media buttons was reduced from 1500ms to 800ms to allow intentional rapid presses on car kits.
- System-level media panels from OEM devices (Samsung, Xiaomi, etc.) are now accepted as valid controllers.

### BREAKING CHANGES
None

### Risks / What to test
- Playback position is saved correctly when stopping the app or receiving a call
- Resume from notification, Bluetooth headset, and Android Auto produces the correct book/chapter
- Global timeline seeking works on multi-chapter audiobooks in Android Auto and car kits
- Favorite toggle works from both the app and remote controllers
- Cover art appears for all source types (local folders, downloads, web sources)

## Русский
- Android Auto теперь предлагает более удобный просмотр с единой вкладкой «Источники», следующей порядку ваших библиотечных вкладок, а страницы источников показывают фильтры (категории, сортировка) перед списком книг.
- Воспроизведение в фоновом режиме стало надёжнее: повторные сигналы гарнитуры, Bluetooth и медиа-кнопок реже вызывают дублирование запусков или потерю команд перемотки, а действия уведомлений более стабильно пробуждают плеер.
- Пульты дистанционного управления и автомобильные системы (Android Auto) теперь показывают настраиваемый ряд кнопок для быстрого доступа к избранному, скорости воспроизведения, пропуску тишины, нормализации громкости и таймеру сна.
- Аудиокниги с несколькими главами теперь отображают корректную общую временную шкалу на Bluetooth-устройствах, автомобильных системах и Android Auto, с кнопками предыдущей/следующей главы в ряду медиа-кнопок.
- Обложки теперь надёжнее отображаются для локальных папок, загрузок и приватных файлов в библиотеке, истории, уведомлениях и Android Auto.
- Приложение теперь дожидается сохранения позиции воспроизведения перед остановкой, поэтому позиция реже теряется при остановке сервиса.
- Сохранённые книги в истории и избранном теперь надёжнее переподключаются к оригинальному источнику, улучшая загрузку обложек и повторное открытие.
- Защищённые ссылки теперь корректно завершаются ошибкой при неправильном пароле вместо отображения искажённого текста.
- Загруженные книги распознаются надёжнее после обновления или перезапуска, включая пересвязанные папки и частичные загрузки.

### Изменения в поведении
- Защитное окно от двойных нажатий для медиа-кнопок уменьшено с 1500 мс до 800 мс, чтобы обеспечить возможность намеренных быстрых нажатий на автомобильных системах.
- Медиа-панели системного уровня от OEM-устройств (Samsung, Xiaomi и др.) теперь принимаются как допустимые контроллеры.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
Нет

### Риски / Что проверить
- Позиция воспроизведения корректно сохраняется при остановке приложения или входящем звонке
- Возобновление из уведомления, Bluetooth-гарнитуры и Android Auto даёт правильную книгу/главу
- Глобальная временная шкала работает для много главных аудиокниг в Android Auto и автомобильных системах
- Переключение избранного работает как из приложения, так и с пультов дистанционного управления
- Обложки отображаются для всех типов источников (локальные папки, загрузки, веб-источники)
