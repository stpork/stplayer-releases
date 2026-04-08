# Release notes — 0.0.47

Release date: 06-Apr-2026 

## English
- **Enhanced Android Auto experience:** Browsing is now faster and more intuitive with a streamlined "Sources" entry that follows your library preferences, and dedicated filters (category, sort) for clearer book discovery.
- **Improved playback reliability:** Background playback is more robust; repeat signals from headsets, Bluetooth devices, and media buttons no longer cause duplicate starts or lost progress.
- **Customizable car controls:** Android Auto and car kits now feature a dedicated button row for quick access to favorite toggles, playback speed, skip silence, loudness normalization, and the sleep timer.
- **Unified audiobook timeline:** Multi-chapter audiobooks now display a consistent global timeline and navigation controls across Bluetooth devices, car systems, and Android Auto.
- **Refined artwork consistency:** Cover art loading is significantly more reliable across the library, history, notifications, and Android Auto, especially for private or downloaded files.
- **Safer shutdown:** The app now ensures pending playback positions are saved before exiting, preventing progress loss on sudden service stops.
- **Improved connection resilience:** Saved items in history and favorites reconnect to original sources more dependably, ensuring artwork loads and files open correctly after restarts.
- **Cleaner error handling:** Accessing protected links with incorrect credentials now fails cleanly, preventing corrupted display or UI hangs.
- **Better download recognition:** Downloaded files are detected more reliably after a refresh, including relinked folders and partial downloads.

### Behavior changes
- Playback controls in external interfaces (Car, Bluetooth) now more faithfully reflect app settings (speed, silence skipping).
- Global timeline support in Android Auto now actively uses internal track metadata to prevent position jumping.

### BREAKING CHANGES
- None

### Risks / What to test
- Verify playback resumption and position persistence after app closure.
- Test Android Auto/car head-unit navigation and artwork display.
- Ensure "Skip Silence" and "Loudness Normalization" toggle states correctly sync between the car interface and the app.

## Русский
- **Улучшенная работа с Android Auto:** Навигация стала быстрее и удобнее: единый раздел «Источники» теперь соответствует вашему порядку в библиотеке, а новые фильтры (категории, сортировка) помогают быстрее находить книги.
- **Повышенная надежность воспроизведения:** Воспроизведение в фоновом режиме стало стабильнее; повторные сигналы от гарнитур, Bluetooth-устройств и кнопок управления больше не приводят к двойному запуску или потере позиции прослушивания.
- **Новое меню быстрого доступа в авто:** На экранах Android Auto и в мультимедийных системах авто появилась специальная панель с кнопками для быстрого управления избранным, скоростью воспроизведения, пропуском тишины, нормализацией громкости и таймером сна.
- **Единая временная шкала для аудиокниг:** Многоглавые аудиокниги теперь корректно отображают общую шкалу времени и кнопки перехода между главами при использовании Bluetooth-устройств, систем автомобиля и Android Auto.
- **Улучшенное отображение обложек:** Обложки книг теперь стабильно подгружаются в библиотеке, истории, уведомлениях и Android Auto, включая локальные папки и защищенные файлы.
- **Безопасное завершение работы:** Приложение гарантирует сохранение прогресса прослушивания перед закрытием, что исключает потерю позиции при внезапной остановке сервиса.
- **Более надежное восстановление сессий:** Книги из истории и избранного быстрее восстанавливают связь с источником, обеспечивая корректное отображение обложек и открытие файлов после перезапуска.
- **Исправленная обработка ошибок:** При вводе неверного пароля к защищенным ссылкам приложение теперь корректно сообщает об ошибке, вместо отображения некорректных данных.
- **Улучшенное распознавание загрузок:** Загруженные книги надежнее обнаруживаются после обновления библиотеки, включая случаи с перепривязанными папками и неполными загрузками.

### Изменения в поведении
- Элементы управления в интерфейсах авто и Bluetooth теперь точнее соответствуют настройкам приложения (скорость, пропуск тишины).
- Глобальная шкала времени в Android Auto теперь активнее использует метаданные треков для предотвращения скачков позиции.

### BREAKING CHANGES
- Нет

### Риски / Что протестировать
- Проверьте возобновление воспроизведения и сохранение позиции после закрытия приложения.
- Проверьте навигацию и отображение обложек через Android Auto или головное устройство автомобиля.
- Убедитесь, что состояния «Пропуск тишины» и «Нормализация громкости» корректно синхронизируются между интерфейсом авто и приложением.
