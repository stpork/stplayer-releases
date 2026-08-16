All changes in this range are bug fixes with clear user impact. Generating the release notes:

# Release notes — 0.0.82

Release date: 16-Aug-2026

## English
- Fixed a rare crash-and-restart loop on some Android 10–12 devices where the app would repeatedly relaunch instead of starting playback.
- Fixed a crash that could occur when resuming playback from an external control (car system, Bluetooth, or a system media panel).
- Fixed missing cover art on the playback notification for some older devices — the book cover, title, and controls now show reliably.
- The notification now consistently shows the current book's title and artwork instead of a generic "Media service" placeholder.
- Fixed a "phantom" paused-media widget appearing on some Xiaomi (MIUI/HyperOS) phones when nothing was actually playing.
- Fixed a crash when opening the folder picker in Settings on devices that lack a built-in file picker (some TVs and stripped-down ROMs); you now get a clear message instead.
- Improved stability of downloaded-book handling when storage access is lost or files are moved — the app repairs itself instead of crashing.

### Behavior changes
- On devices without a system file picker, choosing a download/media folder now shows a "picker unavailable" message rather than failing silently or crashing.
- The playback notification prefers rich content (book title, cover, transport controls) and only falls back to a plain status message when no book is loaded.

### BREAKING CHANGES
- None

### Risks / What to test
- Start, pause, and resume playback via the notification, a car head unit, and Bluetooth controls.
- Confirm the notification shows the book cover and title on Android 10, 11, and 12 devices.
- On Xiaomi/HyperOS devices, confirm no leftover "Paused" widget appears after stopping playback.
- Open Settings → download/media folder picker on a normal phone (should open), and confirm graceful messaging on a device with no file picker.
- Resume a previously downloaded book after revoking and re-granting storage access.

## Русский

# Примечания к выпуску — 0.0.82

Дата выпуска: 16-авг-2026

## Русский
- Исправлен редкий цикл «сбой и перезапуск» на некоторых устройствах Android 10–12, когда приложение перезапускалось вместо начала воспроизведения.
- Исправлен сбой, который мог возникать при возобновлении воспроизведения через внешнее управление (система автомобиля, Bluetooth или системная медиапанель).
- Исправлено отсутствие обложки в уведомлении воспроизведения на некоторых старых устройствах — обложка книги, название и элементы управления теперь отображаются стабильно.
- В уведомлении теперь стабильно показываются название текущей книги и обложка вместо общей надписи-заглушки.
- Исправлен «фантомный» виджет приостановленного воспроизведения на некоторых телефонах Xiaomi (MIUI/HyperOS), когда ничего фактически не воспроизводилось.
- Исправлен сбой при открытии выбора папки в Настройках на устройствах без встроенного файлового менеджера (некоторые ТВ и урезанные прошивки) — теперь показывается понятное сообщение.
- Повышена стабильность работы со скачанными книгами при потере доступа к хранилищу или перемещении файлов — приложение восстанавливается вместо сбоя.

### Изменения в поведении
- На устройствах без системного выбора файлов при выборе папки для загрузок/медиа теперь показывается сообщение «выбор недоступен» вместо тихого сбоя или падения.
- Уведомление воспроизведения предпочитает полноценное содержимое (название книги, обложка, элементы управления) и переходит к простому статусному сообщению только тогда, когда книга не загружена.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
- Нет

### Риски / Что проверить
- Запуск, пауза и возобновление воспроизведения через уведомление, автомобильную магнитолу и элементы управления Bluetooth.
- Убедиться, что в уведомлении отображаются обложка и название книги на устройствах с Android 10, 11 и 12.
- На устройствах Xiaomi/HyperOS убедиться, что после остановки воспроизведения не остаётся виджет «Пауза».
- Открыть Настройки → выбор папки для загрузок/медиа на обычном телефоне (должен открыться) и проверить корректное сообщение на устройстве без файлового менеджера.
- Возобновить ранее скачанную книгу после отзыва и повторного предоставления доступа к хранилищу.
