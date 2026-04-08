# Release notes — 0.0.7

Release date: 10-Feb-2026 

## English
- Fixed refresh reliability in Library/Search/Category views by rebuilding results from a clean state, reducing stale or mixed results after reload.
- Pull-to-refresh is now less accidental: refresh triggers only after a short hold, with a clear visual signal when release will start refresh.
- Improved list responsiveness on large collections by reducing high-frequency state updates that previously caused extra UI churn.
- Improved first-load smoothness by deferring heavy background list work until after initial rendering.
- Artwork loading is now smarter (focused around visible items), improving perceived scrolling smoothness.
- Fixed cases where web item follow-up/detail loading could fail after cache/state resets.
- Tapping the playback notification now opens the player screen more reliably.

### Behavior changes
- Pull down and hold briefly (about 0.3s) before release to trigger refresh.
- During active refresh, empty-state placeholders are suppressed to reduce flicker.
- Refresh now forces a full reload for the current search/category context instead of reusing stale pagination state.
- Tapping the media notification now consistently routes to the active player session.

### BREAKING CHANGES
- None

### Risks / What to test
- Verify pull-to-refresh gesture timing and indicator feedback on real devices.
- Verify refresh correctness in normal list, search results, and category pages (no stale/duplicated merge artifacts).
- Verify notification tap behavior from background/foreground and lock-screen scenarios.
- Verify library scrolling smoothness with large lists and many artworks.
- Verify web source detail loading after cache cleanup/reset flows.

## Русский
- Повышена надежность обновления в Библиотеке/Поиске/Категориях: данные пересобираются «с нуля», что снижает риск устаревших или смешанных результатов после перезагрузки.
- Жест pull-to-refresh стал менее случайным: обновление запускается только после короткого удержания, и есть явный визуальный сигнал, когда отпускание действительно запустит обновление.
- Улучшена отзывчивость списков на больших коллекциях за счет снижения слишком частых обновлений состояния, которые раньше создавали лишнюю нагрузку на UI.
- Улучшена плавность первого отображения списка: тяжелая фоновая обработка откладывается до завершения первичного рендера.
- Загрузка обложек стала более умной (фокус вокруг видимых элементов), из-за чего прокрутка воспринимается плавнее.
- Исправлены случаи, когда у веб-элементов мог сбоить повторный/детальный догруз после очистки кэша или сброса состояния.
- Нажатие на уведомление воспроизведения теперь надежнее открывает экран плеера.

### Изменения поведения
- Для обновления теперь нужно потянуть список вниз и чуть удержать (примерно 0,3 с), затем отпустить.
- Во время активного обновления скрывается пустой placeholder, чтобы убрать визуальное мерцание.
- Обновление теперь принудительно делает полную перезагрузку для текущего контекста поиска/категории, а не использует потенциально устаревшее состояние пагинации.
- Нажатие на медиа-уведомление теперь стабильно переводит в активную сессию плеера.

### BREAKING CHANGES
- None

### Risks / What to test
- Проверьте тайминг жеста pull-to-refresh и визуальную индикацию на реальных устройствах.
- Проверьте корректность обновления в обычном списке, в поиске и в категориях (без устаревших/дублирующихся смешанных результатов).
- Проверьте поведение по нажатию на уведомление из фона/переднего плана и с экрана блокировки.
- Проверьте плавность прокрутки библиотеки на больших списках и при большом количестве обложек.
- Проверьте догруз деталей для веб-источников после сценариев очистки кэша/сброса состояния.