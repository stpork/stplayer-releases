I have the full picture. Now generating the release notes in the user's requested format. Let me note the honest date: the input says release date 04-Aug-2026, but VERSION_CODE-always-+1 convention exists; I'll follow the input's stated date.

Key user-visible themes:
- **Android TV** — massive D-pad/remote overhaul (the bulk of commits): drawer/menu operable by remote, Back behaves correctly, focus never lost, Settings navigable, player controls, cold-launch to player, channel-up/down source switching, crash fixes on Fire TV.
- **Startup** — instant splash + live "Starting up (Xs)" counter.
- **Player UI** — dial dialogs centred/scrollable/width-capped, +/- buttons, tap-moves-cursor, controls always shown.
- **Android Auto** — sources no longer become unreadable in the car; browse failures surfaced; "look at your phone" guidance.
- **Data integrity** — favorites no longer lost; deleted books don't resurrect; playback position/bookmarks preserved on read faults; replay-from-start persists after finishing a book; recover from corrupt settings/config instead of crash-on-launch.
- **Playback** — Bluetooth/remote pause stays paused (no unexpected auto-resume); notification stays alive across all sources; source-switch reliability.
- **Stability** — crash/OOM fixes (large TV grids, torrent parsing), false "tampered app" reports fixed for legitimate installs.
- **Help** — TV D-pad guide rewritten across all languages.

# Release notes — 0.0.78

Release date: 04-Aug-2026

## English
- Android TV remote support overhauled: the source menu, library, book, player and settings are all fully navigable with the D-pad; the focused item is clearly highlighted and the cursor no longer gets lost.
- Back now behaves predictably on TV: it opens/closes the source menu, steps back one screen, and hold-Back exits the app from anywhere.
- Channel Up/Down switches sources on TV, and the app can launch straight into the player when something is already playing.
- Faster-feeling startup: an app-icon splash appears instantly with a live "Starting up (Xs)" counter.
- Player dials (speed, sleep timer) are centred, scrollable, and no longer stretch across wide or landscape screens; added +/- buttons and tap-to-move on the dials, and playback controls now stay visible.
- Android Auto fixes: sources no longer become unreadable in the car, browse errors are shown instead of an empty list, and you get a "look at your phone" hint when a source needs an action there.
- Your data is safer: favorites are no longer lost, deleted books stay deleted, and your position and bookmarks are preserved even if a file can't be read momentarily.
- Replay-from-start now sticks after you finish a book, so restarting a completed title saves progress from the beginning again.
- A Bluetooth or car/remote pause now stays paused instead of unexpectedly resuming.
- The playback notification stays alive while switching between sources.
- The app now recovers automatically from a corrupted settings/config file instead of crashing on launch.
- Fixed crashes and freezes on Android TV (large grids, folder picker) and rare out-of-memory issues, plus false "modified app" warnings for legitimate installs.
- Updated on-screen Help with a full Android TV remote guide in every language.

### Behavior changes
- On TV, Back opens/closes the source menu and steps back a screen; hold Back to exit. Channel Up/Down changes source.
- A pause from Bluetooth or a car/remote is treated as a deliberate pause and will not auto-resume.
- Finishing a book and replaying now restarts from the beginning and saves progress from there.
- If the settings/config file is damaged, the app resets those preferences to defaults on launch (library, positions and history are unaffected).

### BREAKING CHANGES
- None

### Risks / What to test
- Android TV: navigate library, source menu, book, player and settings entirely by remote; confirm focus is always visible, Back and hold-Back work on every screen, and Channel Up/Down switches sources.
- Cold start on a slow device/TV: splash appears immediately and the app reaches a usable state.
- Player dials on phone and in landscape/wide layouts: centred, scrollable, correctly sized.
- Android Auto: sources load in the car after the phone has been backgrounded a while.
- Favorites, delete-a-book, and playback position survive app restarts and transient read errors.
- Bluetooth/car pause stays paused; notification persists across source switches.

## Русский
- Полностью переработана поддержка пульта на Android TV: меню источников, библиотека, книга, плеер и настройки управляются крестовиной; выделенный элемент чётко подсвечивается, а фокус больше не теряется.
- «Назад» на ТВ работает предсказуемо: открывает/закрывает меню источников, возвращает на шаг назад, а удержание «Назад» выходит из приложения с любого экрана.
- Кнопки «Канал +/−» переключают источники на ТВ, а приложение может сразу открываться в плеере, если что-то уже воспроизводится.
- Более быстрый запуск: мгновенная заставка со значком приложения и счётчиком «Запуск (Xс)».
- Диски плеера (скорость, таймер сна) теперь по центру, прокручиваются и не растягиваются на широких и горизонтальных экранах; добавлены кнопки +/− и перемещение касанием, а элементы управления воспроизведением всегда видны.
- Исправления для Android Auto: источники больше не становятся нечитаемыми в машине, ошибки загрузки показываются вместо пустого списка, а при необходимости действия на телефоне выводится подсказка «посмотрите на телефон».
- Данные надёжнее: избранное больше не теряется, удалённые книги не возвращаются, а позиция и закладки сохраняются даже при временной ошибке чтения файла.
- Повтор с начала теперь сохраняется после завершения книги, поэтому при перезапуске завершённой книги прогресс снова пишется с начала.
- Пауза с Bluetooth или из машины/пульта теперь остаётся паузой и не возобновляется сама.
- Уведомление воспроизведения не пропадает при переключении между источниками.
- Приложение автоматически восстанавливается после повреждённого файла настроек/конфигурации вместо сбоя при запуске.
- Исправлены сбои и зависания на Android TV (большие списки, выбор папки) и редкие ошибки нехватки памяти, а также ложные предупреждения о «модифицированном приложении» для легальных установок.
- Обновлена встроенная справка с полным руководством по пульту Android TV на всех языках.

### Изменения поведения
- На ТВ «Назад» открывает/закрывает меню источников и возвращает на шаг назад; удержание «Назад» — выход. «Канал +/−» меняет источник.
- Пауза с Bluetooth или из машины/пульта считается намеренной и не возобновляется автоматически.
- Завершение книги и повтор теперь начинают с начала и сохраняют прогресс оттуда.
- При повреждении файла настроек/конфигурации приложение сбрасывает эти параметры к значениям по умолчанию при запуске (библиотека, позиции и история не затрагиваются).

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
- Нет

### Риски / Что проверить
- Android TV: пройти по библиотеке, меню источников, книге, плееру и настройкам только пультом; убедиться, что фокус всегда виден, «Назад» и удержание «Назад» работают на каждом экране, а «Канал +/−» переключает источники.
- Холодный запуск на медленном устройстве/ТВ: заставка появляется сразу, приложение доходит до рабочего состояния.
- Диски плеера на телефоне и в горизонтальной/широкой раскладке: по центру, прокручиваются, правильного размера.
- Android Auto: источники загружаются в машине после того, как телефон долго был в фоне.
- Избранное, удаление книги и позиция воспроизведения сохраняются при перезапусках и временных ошибках чтения.
- Пауза с Bluetooth/из машины остаётся паузой; уведомление сохраняется при переключении источников.
