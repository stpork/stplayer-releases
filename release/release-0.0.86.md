# Release notes — 0.0.86

Release date: 09-Sep-2026

## English

- Added voice search on devices with speech recognition support.
- Improved playback resume and protection against unexpected restarts after headphones disconnect or another app takes over audio.
- Fixed the playback position display after seeking while paused.
- Improved saving and restoring listening progress and per-book audio settings.
- Fixed sync issues that could bring back deleted books or leave recent changes unsent.
- Backup merging now preserves your existing ignore list, and audio settings transfer more reliably.
- Improved search navigation: Back restores your original query and results, and failed pages remain available to retry.
- Cancelling a stalled download now stops the request promptly.
- Improved torrent playback while downloading, including seeking into unfinished sections and recognising already downloaded content.
- Improved Android Auto browsing reliability while playback is idle.
- Improved TV remote focus and long-press menus.
- Added clearer, translated messages for connection, backup and sync errors.

### Behavior changes

- Voice input fills the search field and submits the recognised query; the magnifier submits typed text.
- On supported media controllers, a short Next/Previous press switches chapters when released; holding seeks without first switching chapters.
- On TV, Channel Up/Down moves one page through the current book grid. Use the source menu to switch sources.

### BREAKING CHANGES

None

### Risks / What to test

- [ ] Upgrade from 0.0.85 and check saved progress, favourites and per-book audio settings.
- [ ] Check screen-off playback, Bluetooth controls, headphone disconnection and Android Auto browsing.
- [ ] Test voice search, Back navigation and retrying search pages after a connection failure.
- [ ] Sync additions and deletions between devices; restore a backup using Merge.
- [ ] Cancel and resume downloads, including while playing the same torrent book; check recovery after restoring folder access.
- [ ] Check TV focus, long-press menus and Channel Up/Down paging.

## Русский

- Добавлен голосовой поиск на устройствах с поддержкой распознавания речи.
- Улучшено возобновление воспроизведения и защита от неожиданного запуска после отключения наушников или перехвата звука другим приложением.
- Исправлено отображение позиции после перемотки на паузе.
- Повышена надёжность сохранения и восстановления позиции прослушивания и настроек звука для отдельных книг.
- Исправлены ошибки синхронизации, из-за которых удалённые книги могли возвращаться, а последние изменения — не отправляться.
- Объединение с резервной копией теперь сохраняет ваш список игнорирования; настройки звука переносятся надёжнее.
- Улучшена навигация в поиске: кнопка «Назад» возвращает исходный запрос и результаты, а страницы, не загрузившиеся из-за ошибки, можно загрузить повторно.
- Отмена зависшей загрузки теперь своевременно прерывает запрос.
- Улучшено воспроизведение торрентов во время загрузки, включая перемотку к ещё не загруженным фрагментам и распознавание уже скачанного содержимого.
- Повышена надёжность просмотра библиотеки в Android Auto, когда воспроизведение не запущено.
- Улучшены навигация пультом на телевизоре и меню по долгому нажатию.
- Добавлены более понятные переведённые сообщения об ошибках подключения, резервного копирования и синхронизации.

### Изменения в поведении

- Голосовой ввод заполняет строку поиска и сразу запускает поиск; кнопка с лупой отправляет введённый текст.
- На поддерживаемых устройствах управления короткое нажатие «Следующий/Предыдущий» переключает главу при отпускании кнопки; удержание выполняет перемотку без предварительного переключения главы.
- На телевизоре кнопки переключения каналов вверх/вниз перелистывают текущую сетку книг на одну страницу. Для смены источника используйте меню источников.

### НЕСОВМЕСТИМЫЕ ИЗМЕНЕНИЯ

Нет

### Риски / Что проверить

- [ ] Обновиться с 0.0.85 и проверить сохранённые позиции, избранное и настройки звука отдельных книг.
- [ ] Проверить воспроизведение с выключенным экраном, управление по Bluetooth, отключение наушников и просмотр библиотеки в Android Auto.
- [ ] Проверить голосовой поиск, возврат кнопкой «Назад» и повторную загрузку страниц поиска после сбоя соединения.
- [ ] Проверить синхронизацию добавлений и удалений между устройствами и восстановление резервной копии в режиме объединения.
- [ ] Проверить отмену и возобновление загрузок, в том числе во время прослушивания той же торрент-книги, а также восстановление работы после возврата доступа к папке.
- [ ] Проверить перемещение фокуса на телевизоре, меню по долгому нажатию и перелистывание кнопками каналов.