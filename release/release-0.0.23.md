# Release notes — 0.0.23

Release date: 21-Feb-2026

## English

### New features and improvements
- **More sort options for local files:** Sort your local audiobooks and folders by Recent, Title, Author, Performer, Duration, or Date. The default sort is now "Recent" so your newest content appears first.
- **Smoother animations:** The download progress spinner now uses GPU-accelerated rendering, eliminating stutter during downloads.
- **Faster image loading:** Broken or unavailable cover images are now remembered during your session, preventing repeated loading attempts that caused flickering.

### Bug fixes
- **Improved stability:** Added safety limits to prevent crashes when encountering unusually large metadata files or network responses.
- **Better pagination:** Fixed URL construction issues that could cause browsing pages to fail on some sources.
- **More reliable source selection:** The app now correctly restores your last-selected source on startup.

### BREAKING CHANGES
None

### Risks / What to test
- Browse local files and verify all sort options work correctly
- Download content and check that progress spinner animates smoothly
- Switch between sources and confirm the app remembers your selection after restart
- Test browsing various sources (BYT, ABM, PLK, etc.) for pagination reliability

---

## Русский

### Новые возможности и улучшения
- **Больше параметров сортировки для локальных файлов:** Сортируйте локальные аудиокниги и папки по дате добавления, названию, автору, исполнителю, длительности или году. По умолчанию теперь используется сортировка «По дате» — новый контент отображается первым.
- **Плавная анимация:** Индикатор прогресса загрузки теперь использует GPU-ускорение, что устраняет подтормаживания во время загрузок.
- **Быстрая загрузка изображений:** Недоступные обложки запоминаются в течение сессии, предотвращая повторные попытки загрузки, которые вызывали мерцание.

### Исправления ошибок
- **Повышенная стабильность:** Добавлены ограничения безопасности для предотвращения сбоев при обработке unusually больших файлов метаданных или сетевых ответов.
- **Улучшенная постраничная навигация:** Исправлены проблемы с построением URL, которые могли приводить к сбоям при просмотре страниц на некоторых источниках.
- **Более надёжный выбор источника:** Приложение теперь корректно восстанавливает последний выбранный источник при запуске.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
Отсутствуют

### Риски / Что тестировать
- Просмотрите локальные файлы и проверьте, что все параметры сортировки работают корректно
- Загрузите контент и убедитесь, что индикатор прогресса анимируется плавно
- Переключайтесь между источниками и подтвердите, что приложение запоминает ваш выбор после перезапуска
- Протестируйте навигацию по различным источникам (BYT, ABM, PLK и др.) на надёжность постраничного просмотра
