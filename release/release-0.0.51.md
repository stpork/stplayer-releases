# Release notes — 0.0.51

Release date: 11-Apr-2026

## English

- **Android Auto: seek controls overhaul** — standard prev/rew/play/fwd/next transport buttons now work correctly; added ±30s fine-seek buttons in overflow menu; rewind/forward commands now seek ±3 minutes as intended.
- **Notification controls redesigned** — consolidated to 5 buttons with correct compact view showing Rewind / Play / Forward instead of the previous incorrect button order.
- **Bluetooth / headset long-press seek** — long-pressing skip buttons on Bluetooth headsets now seeks within the current track instead of jumping to the next chapter.
- **Haptic feedback fixed** — playback controls now give a short vibration on tap, a longer one on hold, and no spurious vibration on release.
- **Sorting improvements** — "Today first" is now the default sort; sort preferences are remembered per source and category.
- **Local/SAF source improvements** — source name now displays correctly from configuration; storage access status shows in red when permission is missing.
- **Fixed playback for KVH source** — resolved a regex compatibility issue that prevented audio from loading.
- **Fixed broken content parsing** for several sources (ABM, AKV, SLV, AKO, RTR) caused by corrupted regex patterns.
- **Fixed crash on empty playback resume** — app no longer crashes when resuming a session with no saved position data.
- **Fixed rare playback interruptions** — resolved a race condition where concurrent operations could drop position-save requests or cause errors with empty playlists.
- **Background playback battery & memory improvements** — reduced battery drain and memory usage during background listening by releasing artwork caches, HTTP connections, and metadata caches when the system is under memory pressure (~3MB+ freed).
- **Faster SAF folder scanning** — optimized file lookup for locally stored audiobooks on external storage.
- **Android Auto now syncs source selection** with the phone app when started via Bluetooth or Auto.

### Behavior changes
- Default sort order is now "Today first" instead of the previous default. Existing per-source sort preferences are preserved.
- Notification controls reduced from 7 to 5 buttons; compact view shows Rewind/Play/Forward.
- Android Auto rewind/forward buttons now seek ±3 minutes (previously ±30 seconds).

### BREAKING CHANGES
None

### Risks / What to test
- Verify notification buttons work correctly on Android 13+ and older versions (tap each button).
- Test Android Auto: browse, play, seek with transport buttons and overflow ±30s buttons.
- Test Bluetooth headset: play/pause, short press skip, long press skip (should seek).
- Verify playback resume after app kill (cold start resume).
- Verify sort order persists after switching sources and categories.
- Verify local/SAF audiobook playback and folder discovery.
- Test background playback stability over 30+ minutes — check battery usage.
- Verify KVH, ABM, AKV, SLV, AKO, RTR sources load and play content.

---

## Русский

- **Android Auto: обновление управления перемоткой** — стандартные кнопки транспорта (назад/перемотка/воспроизведение/вперёд/далее) теперь работают корректно; добавлены кнопки точной перемотки ±30 сек в дополнительном меню; перемотка вперёд/назад теперь сдвигает на ±3 минуты, как задумано.
- **Переработаны элементы управления в уведомлении** — количество кнопок сокращено до 5, в компактном виде корректно отображаются «Назад / Воспроизведение / Вперёд» вместо прежнего неправильного порядка.
- **Перемотка долгим нажатием на Bluetooth-гарнитуре** — долгое нажатие кнопок переключения на Bluetooth-гарнитуре теперь перематывает внутри текущего трека, а не переходит к следующей главе.
- **Исправлена тактильная отдача** — элементы управления воспроизведением теперь дают короткую вибрацию при нажатии, длинную при удержании и не вибрируют при отпускании.
- **Улучшения сортировки** — «Сначала сегодняшние» теперь выбрано по умолчанию; настройки сортировки сохраняются для каждого источника и категории.
- **Улучшения локального/SAF-источника** — название источника теперь корректно отображается из конфигурации; статус доступа к хранилищу выделяется красным при отсутствии разрешения.
- **Исправлено воспроизведение источника KVH** — устранена проблема совместимости регулярных выражений, из-за которой аудио не загружалось.
- **Исправлен парсинг контента** для нескольких источников (ABM, AKV, SLV, AKO, RTR), вызванный повреждёнными регулярными выражениями.
- **Исправлен вылет при пустом возобновлении воспроизведения** — приложение больше не падает при возобновлении сессии без сохранённой позиции.
- **Исправлены редкие прерывания воспроизведения** — устранено состояние гонки, при котором параллельные операции могли терять запросы на сохранение позиции или вызывать ошибки с пустыми плейлистами.
- **Оптимизация батареи и памяти при фоновом воспроизведении** — снижен расход батареи и памяти при фоновом прослушивании за счёт освобождения кешей обложек, HTTP-соединений и кешей метаданных при нехватке памяти (высвобождается ~3 МБ+).
- **Ускорено сканирование SAF-папок** — оптимизирован поиск файлов для аудиокниг на внешнем хранилище.
- **Android Auto теперь синхронизирует выбор источника** с приложением на телефоне при подключении через Bluetooth или Auto.

### Изменения поведения
- Сортировка по умолчанию теперь «Сначала сегодняшние» вместо прежней. Ранее сохранённые настройки сортировки по источникам сохраняются.
- Количество кнопок в уведомлении сокращено с 7 до 5; в компактном виде отображаются «Назад/Воспроизведение/Вперёд».
- Кнопки перемотки в Android Auto теперь сдвигают на ±3 минуты (ранее ±30 секунд).

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
Нет

### Риски / Что проверить
- Проверить кнопки уведомления на Android 13+ и более ранних версиях (нажать каждую кнопку).
- Протестировать Android Auto: навигация, воспроизведение, перемотка кнопками транспорта и кнопками ±30 сек в дополнительном меню.
- Протестировать Bluetooth-гарнитуру: воспроизведение/пауза, короткое нажатие переключения, долгое нажатие (должна быть перемотка).
- Проверить возобновление воспроизведения после завершения приложения (холодный старт).
- Проверить сохранение порядка сортировки при переключении источников и категорий.
- Проверить воспроизведение и обнаружение папок локальных/SAF-аудиокниг.
- Протестировать стабильность фонового воспроизведения более 30 минут — проверить расход батареи.
- Проверить источники KVH, ABM, AKV, SLV, AKO, RTR — загрузка и воспроизведение контента.
