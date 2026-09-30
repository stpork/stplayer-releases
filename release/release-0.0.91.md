# Release notes — 0.0.91

Release date: 01-Oct-2026

## English

- More reliable resume when chapter lengths are unknown, with saved playback speed preserved when replaying a book.
- Cancelled or delayed playback requests no longer override a newer book selection or start playback after Pause or Stop.
- Improved restarting of books stored in local folders, keeping the full book available.
- More consistent playback controls across the app, remotes, headsets and Android Auto.
- Added separate Faster, Slower and Reset speed controls for Android Auto and compatible Bluetooth displays.
- Improved recovery from expired streaming links, preventing recovery from selecting the wrong chapter.
- Fixed excessive automatic catalogue loading that could unexpectedly shift the displayed books.
- Clearer playback feedback: a loading message while waiting for network data, and translated error descriptions with codes when available.

### Behavior changes

- Play works for the selected book regardless of automatic resume settings. Automatic starts and external restoration still respect those settings. Holding Play/Pause switches playback state only once.
- Android Auto and Bluetooth controls now prioritise 30-second skips. Three-minute skips remain in additional controls and replace chapter buttons for single-track books.
- Each speed-button tap changes speed by 0.1×, stopping at the limits. A separate button restores 1.00× without changing your position or starting paused playback.
- Remote playback displays now show the current chapter’s time adjusted for playback speed, rather than the whole book’s timeline. The chapter subtitle includes speed and playback status.

### BREAKING CHANGES

- Android Auto and Bluetooth control menus no longer offer shortcuts for favourites, skipping silence, volume normalisation or the sleep timer.

### Risks / What to test

- Resume partially listened books, including books with unknown chapter lengths; replay completed books and check saved progress and speed.
- Switch books or press Pause/Stop during loading; confirm no delayed playback starts.
- Check headset and TV remote buttons, including long presses, and Android Auto seeking and speed controls on a real device.
- Interrupt streaming, reconnect and confirm playback returns to the same chapter and position.
- Browse, scroll and refresh catalogues; check that pages load without unexpected jumps.

## Русский

- Улучшено возобновление воспроизведения, когда длительность отдельных глав неизвестна; при повторном прослушивании сохраняется выбранная скорость.
- Отменённые или запоздавшие запросы воспроизведения больше не подменяют новую выбранную книгу и не запускают звук после паузы или остановки.
- Улучшен повторный запуск книг из локальных папок: для прослушивания остаётся доступна вся книга.
- Управление воспроизведением стало согласованнее в приложении, с пульта, гарнитуры и через Android Auto.
- Добавлены отдельные кнопки «Быстрее», «Медленнее» и сброса скорости для Android Auto и совместимых Bluetooth-дисплеев.
- Улучшено восстановление воспроизведения при истечении срока действия ссылки: исключён выбор другой главы при восстановлении.
- Исправлена избыточная автоматическая подгрузка каталога, из-за которой показанные книги могли неожиданно смещаться.
- Более понятные сообщения плеера: ожидание данных из сети сопровождается надписью о загрузке, а ошибки — переведённым описанием и кодом, если он доступен.

### Изменения в поведении

- Кнопка воспроизведения запускает выбранную книгу независимо от настроек автоматического возобновления. Автоматический запуск и восстановление по внешней команде по-прежнему учитывают эти настройки. Удержание кнопки воспроизведения/паузы переключает состояние только один раз.
- В Android Auto и Bluetooth приоритет отдан перемотке на 30 секунд. Перемотка на три минуты доступна среди дополнительных кнопок, а для книг с одним треком занимает место кнопок перехода между главами.
- Каждое нажатие кнопки скорости меняет её на 0,1× без перехода по кругу на границах диапазона. Отдельная кнопка возвращает скорость 1,00×, сохраняя позицию и не снимая воспроизведение с паузы.
- На внешних дисплеях теперь показывается время текущей главы с учётом скорости воспроизведения вместо шкалы всей книги. В подписи главы указаны скорость и состояние воспроизведения.

### НЕСОВМЕСТИМЫЕ ИЗМЕНЕНИЯ

- В меню управления Android Auto и Bluetooth больше нет кнопок избранного, пропуска тишины, нормализации громкости и таймера сна.

### Риски / Что проверить

- Возобновление недослушанных книг, включая книги с неизвестной длительностью глав; повторное прослушивание завершённых книг с проверкой сохранения позиции и скорости.
- Смену книги, паузу и остановку во время загрузки: воспроизведение не должно запускаться с задержкой.
- Кнопки гарнитуры и телевизионного пульта, включая удержание; перемотку и настройку скорости в Android Auto на реальном устройстве.
- Восстановление после обрыва сети: воспроизведение должно продолжиться с той же главы и позиции.
- Просмотр, прокрутку и обновление каталогов: страницы должны подгружаться без неожиданных скачков.