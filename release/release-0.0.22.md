# Release notes — 0.0.22

Release date: 20-Feb-2026

## English

- **Enhanced BYT browsing:** Added new Audiobooks category with improved search and sorting options including Popular, Rating, and filters for media-only or playlists-only results.
- **Higher quality cover artwork:** Cover images now save at 1280px (up from 512px) for sharper display on modern devices.
- **New languages:** Added Japanese, Turkish, and Chinese translations.
- **Improved source management:** Sources can now be enabled, disabled, and reordered from Settings. Sort and filter preferences are saved per source.
- **Backup and restore:** Added export/import for source configuration to easily backup or transfer settings.
- **Better startup reliability:** App more consistently restores the last-opened source and library view on launch.
- **UI refinements:** Smoother theme switching, improved library screen responsiveness, and polished mini-player display.

### Behavior changes
- Sort and filter selections in BYT sources now persist between sessions
- Cover images saved to disk are larger (1280px) for better quality on high-density displays
- Source order in the library tab reflects saved preferences rather than default order

### BREAKING CHANGES
None

### Risks / What to test
- BYT browsing: try different sort options (New, Popular, Rating) and filters (All, Media only, Playlists only)
- Source management: reorder sources, disable/enable, verify persistence after app restart
- Backup/restore: export settings, modify, import, verify restoration
- Cover images: download new content and verify saved covers are high resolution
- New languages: switch to Japanese, Turkish, or Chinese and verify UI strings

---

## Русский

- **Улучшен просмотр BYT:** Добавлена новая категория «Аудиокниги» с расширенным поиском и сортировкой, включая «По популярности», «По рейтингу» и фильтры для показа только медиа или плейлистов.
- **Обложки высокого качества:** Обложки теперь сохраняются в разрешении 1280px (ранее 512px) для чёткого отображения на современных устройствах.
- **Новые языки:** Добавлены переводы на японский, турецкий и китайский языки.
- **Улучшенное управление источниками:** Источники теперь можно включать, отключать и менять порядок в настройках. Настройки сортировки и фильтров сохраняются для каждого источника.
- **Резервное копирование и восстановление:** Добавлен экспорт/импорт конфигурации источников для удобного резервного копирования или переноса настроек.
- **Надёжный запуск:** Приложение более последовательно восстанавливает последний открытый источник и вид библиотеки при запуске.
- **Улучшения интерфейса:** Плавное переключение тем, улучшена отзывчивость экрана библиотеки, улучшен отображение мини-плеера.

### Изменения поведения
- Выбор сортировки и фильтров в источниках BYT сохраняется между сессиями
- Обложки, сохраняемые на диск, имеют больший размер (1280px) для лучшего качества на дисплеях высокой плотности
- Порядок источников на вкладке библиотеки отражает сохранённые настройки, а не порядок по умолчанию

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
Нет

### Риски / Что тестировать
- Просмотр BYT: попробуйте разные варианты сортировки (Новые, Популярные, По рейтингу) и фильтры (Все, Только медиа, Только плейлисты)
- Управление источниками: измените порядок источников, отключите/включите, проверьте сохранение после перезапуска приложения
- Резервное копирование: экспортируйте настройки, измените, импортируйте, проверьте восстановление
- Обложки: загрузите новый контент и проверьте, что сохранённые обложки имеют высокое разрешение
- Новые языки: переключитесь на японский, турецкий или китайский и проверьте строки интерфейса
