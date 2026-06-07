# Release notes — 0.0.64

Release date: 07-Jun-2026

## English

- Fixed a crash that could occur on device boot when recently played media was loaded by the system.
- Fixed an issue where the top bar could overlap with the status bar on devices using edge-to-edge display mode.
- Fixed playback position not being saved correctly on the first pause immediately after opening a book (a race condition on cold start).
- Fixed a rare data corruption issue where the wrong book's saved position could be read from disk.
- Fixed downloading failures that could silently occur when the download folder was temporarily unavailable (e.g. after the folder was deleted from a file manager while a storage permission was still active) — the app now recovers gracefully instead of crashing.
- Removed a source's "Authors" browse category that was returning errors (404), preventing the category list from loading correctly.
- Improved playback reliability for multi-track books: track durations are now stored correctly, which fixes global progress percentage and long-press skip-to-end behavior.
- Faster response when loading and checking download statuses (file reads are now streamed instead of loaded fully into memory).
- Several internal regex patterns are now compiled once and reused, reducing CPU overhead during scraping and HLS download processing.

### Behavior changes

- Download folder errors are handled more gracefully: a temporarily inaccessible folder no longer disrupts the library — the app retries on the next scan instead of clearing the storage permission.

### BREAKING CHANGES

None

### Risks / What to test

- Boot the device and verify recently played books appear correctly in the media session.
- Open a book and pause immediately — confirm position is saved and resume works correctly.
- Browse a source's category list — verify no loading errors appear.
- Download a multi-track book; check that the global progress bar reflects the correct percentage and long-press next skips to the end of the book.
- Move or delete a download folder from a file manager, then return to the app — verify the library loads without crashing and does not lose the storage permission.
- Verify the top bar does not overlap the status bar on a device with edge-to-edge display.

---

## Русский

- Исправлен краш, который мог возникать при загрузке устройства, когда система восстанавливала недавно воспроизводимые медиа.
- Исправлено перекрытие верхней панели и строки состояния на устройствах с режимом отображения «от края до края».
- Исправлена ошибка, при которой позиция воспроизведения не сохранялась корректно при первой паузе сразу после открытия книги (состояние гонки при холодном старте).
- Исправлена редкая ошибка, при которой с диска могла считываться сохранённая позиция не той книги.
- Исправлены сбои при скачивании, возникавшие при временной недоступности папки загрузок (например, если папка была удалена из файлового менеджера при активном разрешении на хранилище) — приложение теперь восстанавливается корректно, а не падает.
- Удалена категория «Авторы» одного из источников, которая возвращала ошибку 404 и мешала корректной загрузке списка категорий.
- Улучшена надёжность воспроизведения многотрековых книг: длительность треков теперь сохраняется корректно, что исправляет работу глобального прогресс-бара и long-press перехода к концу книги.
- Ускорена загрузка и проверка статусов скачивания (файлы теперь читаются потоком, а не загружаются целиком в память).
- Ряд внутренних регулярных выражений теперь компилируется один раз и переиспользуется, снижая нагрузку на процессор при парсинге и обработке HLS-загрузок.

### Изменения поведения

- Ошибки с папкой загрузок обрабатываются корректнее: временно недоступная папка больше не нарушает работу библиотеки — приложение повторит попытку при следующем сканировании, не сбрасывая разрешение на хранилище.

### BREAKING CHANGES

Нет

### Риски / Что протестировать

- Перезагрузить устройство и убедиться, что недавно воспроизводимые книги отображаются корректно в медиасессии.
- Открыть книгу и сразу поставить на паузу — убедиться, что позиция сохранилась и возобновление работает правильно.
- Просмотреть список категорий источника — убедиться, что ошибок загрузки нет.
- Скачать многотрековую книгу; проверить, что глобальный прогресс-бар отображает верный процент, а long-press «следующий трек» переходит к концу книги.
- Переместить или удалить папку загрузок через файловый менеджер, затем вернуться в приложение — убедиться, что библиотека загружается без краша и не теряет разрешение на хранилище.
- Убедиться, что верхняя панель не перекрывает строку состояния на устройстве с отображением «от края до края».
