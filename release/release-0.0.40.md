# Release notes — 0.0.40

Release date: 27-Mar-2026 

## English
- Infinite scrolling in library lists is reliable again, so browsing no longer gets stuck after the first page.
- LibriVox now supports author search, and later pages load correctly when you keep browsing results.
- LoyalBooks now has clearer top-level entry points for Audiobooks and Genres.
- More supported sources now offer richer search and browse options, including more author, performer, genre, and playlist-focused searches where available.
- History and library screens feel smoother on low-memory devices, with less unnecessary work while lists update.
- Returning to the app from the background is less likely to trigger a full reload of library content.
- Text scaling now follows your selected UI size more consistently across the app.

### Behavior changes
- Library pagination now keeps loading additional pages instead of sometimes stopping early.
- Some sources now show new browse sections and extra search types when supported.
- UI scale changes now affect text sizing more consistently.
- Returning from the background should preserve more on-screen state and feel faster.

### BREAKING CHANGES
- None

### Risks / What to test
- Browse several long lists and confirm page 2, 3, and later pages load reliably.
- In LibriVox, search by author and continue paging through results.
- In LoyalBooks and other supported sources, verify the new browse sections and source-specific search types.
- Change UI scale and check text sizing across library, player, and settings screens.
- On a low-memory device, or after sending the app to the background, return to library and history screens and confirm they restore quickly without unnecessary reloads.

## Русский
- Бесконечная подгрузка списков в библиотеке снова работает надежно, поэтому просмотр больше не застревает после первой страницы.
- В LibriVox появился поиск по авторам, а при дальнейшем просмотре результатов корректно загружаются следующие страницы.
- В LoyalBooks появились более понятные верхнеуровневые разделы Audiobooks и Genres.
- В большем числе поддерживаемых источников стали доступны расширенные варианты поиска и навигации, включая более точный поиск по авторам, исполнителям, жанрам и плейлистам там, где это поддерживается.
- На устройствах с небольшим объемом памяти экраны истории и библиотеки работают плавнее и делают меньше лишней работы при обновлении списков.
- После возврата в приложение из фона библиотека реже перезагружается полностью.
- Масштаб текста теперь заметно стабильнее следует выбранному размеру интерфейса по всему приложению.

### Изменения поведения
- Подгрузка следующих страниц в библиотеке теперь продолжает работать там, где раньше могла неожиданно остановиться.
- В некоторых источниках появились новые разделы просмотра и дополнительные типы поиска, если они поддерживаются.
- При смене масштаба интерфейса размер текста применяется более последовательно.
- При возврате из фона приложение старается сохранить больше состояния экрана, поэтому работа ощущается быстрее.

### Ломающие изменения
- Нет

### Риски / Что проверить
- Откройте несколько длинных списков и убедитесь, что 2-я, 3-я и следующие страницы загружаются стабильно.
- В LibriVox выполните поиск по автору и проверьте переход по следующим страницам результатов.
- В LoyalBooks и других поддерживаемых источниках проверьте новые разделы просмотра и дополнительные типы поиска.
- Измените масштаб интерфейса и проверьте размер текста в библиотеке, плеере и настройках.
- На устройстве с небольшим объемом памяти, либо после отправки приложения в фон, вернитесь на экраны библиотеки и истории и убедитесь, что они восстанавливаются быстро и без лишней перезагрузки.