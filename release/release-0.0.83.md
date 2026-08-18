The input file has everything I need. The dominant change is a big new **Sync** feature; smaller items are playback fix, TV D-pad fixes, a crash fix, and a player display improvement.

The user's requested output format overrides the skill's Google Play/RuStore format — I'll follow the user's format exactly.

# Release notes — 0.0.83

Release date: 18-Aug-2026

## English

- **New: cross-device sync.** Keep your library the same across all your devices — history, playback positions, favourites, bookmarks and ignore lists. No account needed and fully private: your data is end-to-end encrypted.
- Setting up is simple: create an 8-character code on one device and enter it on the others. Sharing that code is all it takes to join your own group.
- Syncing happens on its own in the background at startup and when you tap Refresh on the Library screen — and it never pauses or jumps the book you're currently listening to.
- Deletions now travel between devices too: remove a book, un-favourite something, or delete a bookmark on one device and it clears on the others.
- You can start a fresh group by regenerating your code, or turn sync off on a device at any time — your library stays put and other devices are unaffected.
- A Privacy Policy link was added to Help, explaining what the app stores and what leaves your device.
- The player now shows position and remaining time adjusted for your playback speed, so the time left matches how long you'll actually listen.
- Fixed a rare startup crash that could leave the app unable to launch after an unexpected shutdown.
- Playback is more reliable when resuming from a saved book: stream links are refreshed before starting, avoiding "can't play" errors from stale links.
- An external play/pause button no longer starts a random book when nothing is loaded.
- TV improvements: Help is now fully usable with the D-pad and closes with Back; the book menu opens ready for D-pad navigation; selecting a book on your remote reliably opens the player; and back-button behaviour is more consistent across devices.

### Behavior changes

- Library sync runs automatically at startup and when you pull-to-refresh or tap Refresh; it can also be triggered manually via "Sync now".
- Removing a book, favourite, category or bookmark on one device will now remove it on your other synced devices.
- Turning sync off on a device no longer erases the shared group data — your other devices keep syncing.
- Player time display now reflects playback speed rather than raw track time.

### BREAKING CHANGES

- None

### Risks / What to test

- Set up sync between two devices; confirm history, positions, favourites, bookmarks and ignore lists converge.
- Verify deletions (book, favourite, category, bookmark) propagate across devices.
- Confirm an active playback session is never interrupted by a sync.
- Test regenerating a code, joining with a code, and turning sync off — check other devices are unaffected.
- Restart the app repeatedly and after force-close to confirm no startup crash and no settings loss.
- Resume a previously saved book and confirm playback starts without stale-link errors.
- On TV: navigate Help, the book menu, and playback entirely with the D-pad; verify Back behaves consistently.
- Check the player's displayed position/remaining time at non-1× speeds.

## Русский

## Русский

- **Новое: синхронизация между устройствами.** Держите библиотеку одинаковой на всех своих устройствах — историю, позиции воспроизведения, избранное, закладки и списки игнорирования. Аккаунт не нужен, и всё приватно: данные защищены сквозным шифрованием.
- Настройка простая: создайте 8-значный код на одном устройстве и введите его на остальных. Этого кода достаточно, чтобы присоединиться к своей группе.
- Синхронизация выполняется сама в фоне при запуске и при нажатии «Обновить» на экране Библиотеки — и никогда не ставит на паузу и не перематывает книгу, которую вы сейчас слушаете.
- Удаления теперь тоже передаются между устройствами: удалите книгу, снимите избранное или удалите закладку на одном устройстве — это применится и на остальных.
- Можно начать новую группу, сгенерировав новый код, или отключить синхронизацию на устройстве в любой момент — библиотека остаётся на месте, другие устройства не затрагиваются.
- В Справку добавлена ссылка на Политику конфиденциальности с описанием того, что приложение хранит и что покидает ваше устройство.
- Плеер теперь показывает позицию и оставшееся время с учётом скорости воспроизведения, поэтому оставшееся время соответствует реальной длительности прослушивания.
- Исправлен редкий сбой при запуске, из-за которого приложение могло не открыться после неожиданного выключения.
- Воспроизведение стало надёжнее при возобновлении сохранённой книги: ссылки на поток обновляются перед началом, что убирает ошибки «не удаётся воспроизвести» из-за устаревших ссылок.
- Внешняя кнопка play/pause больше не запускает случайную книгу, когда ничего не загружено.
- Улучшения для ТВ: Справкой теперь полностью можно управлять с пульта и закрывать кнопкой «Назад»; меню книги открывается готовым к навигации пультом; выбор книги на пульте надёжно открывает плеер; поведение кнопки «Назад» стало единообразнее на разных устройствах.

### Изменения в поведении

- Синхронизация библиотеки запускается автоматически при старте и при жесте «потянуть для обновления» или нажатии «Обновить»; её также можно запустить вручную через «Синхронизировать сейчас».
- Удаление книги, избранного, категории или закладки на одном устройстве теперь удаляет их и на других синхронизированных устройствах.
- Отключение синхронизации на устройстве больше не стирает общие данные группы — остальные устройства продолжают синхронизироваться.
- Отображение времени в плеере теперь учитывает скорость воспроизведения, а не «сырое» время дорожки.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ

- Нет

### Риски / Что протестировать

- Настройте синхронизацию между двумя устройствами; проверьте, что история, позиции, избранное, закладки и списки игнорирования сходятся.
- Убедитесь, что удаления (книга, избранное, категория, закладка) передаются между устройствами.
- Подтвердите, что активное воспроизведение никогда не прерывается синхронизацией.
- Проверьте генерацию нового кода, подключение по коду и отключение синхронизации — убедитесь, что другие устройства не затронуты.
- Многократно перезапустите приложение и после принудительного закрытия — убедитесь в отсутствии сбоя при запуске и потери настроек.
- Возобновите ранее сохранённую книгу и убедитесь, что воспроизведение стартует без ошибок из-за устаревших ссылок.
- На ТВ: пройдите Справку, меню книги и воспроизведение полностью с пульта; проверьте единообразие кнопки «Назад».
- Проверьте отображаемые позицию/оставшееся время в плеере на скоростях, отличных от 1×.
