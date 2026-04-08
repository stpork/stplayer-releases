# Release notes — 0.0.6

Release date: 09-Feb-2026 

## English
- Improved Library screen responsiveness, with smoother scrolling and fewer UI stalls on large lists.
- Artwork and item metadata now load in a more viewport-aware way, so visible content fills in more consistently while you browse.
- Pull-to-refresh now gives clearer feedback and is less prone to accidental triggers.
- Refresh behavior is more stable: existing items stay visible during refresh instead of briefly dropping to an empty state.
- Search flow is more predictable on remote sources: empty search input no longer triggers remote search behavior.

### Behavior changes
- Pull-to-refresh now requires a short hold before release to trigger refresh.
- Refresh keeps the current list visible while new data is loading.
- Remote search mode activates only when a non-empty query is entered.

### BREAKING CHANGES
- None

### Risks / What to test
- Verify pull-to-refresh triggers only after a deliberate short hold.
- Verify list content does not flash to empty during refresh.
- Verify empty search input shows normal browsing results on remote sources.
- Verify cover art and status indicators update correctly while scrolling long lists.

## Русский
- Улучшена отзывчивость экрана Библиотеки: прокрутка стала плавнее, а подвисаний на больших списках стало меньше.
- Загрузка обложек и метаданных стала лучше учитывать видимую область экрана, поэтому контент заполняется стабильнее во время просмотра.
- Обновление «потяни, чтобы обновить» теперь дает более понятную обратную связь и реже срабатывает случайно.
- Поведение обновления стало стабильнее: текущие элементы остаются на экране во время обновления и не исчезают во временно пустое состояние.
- Поиск на удаленных источниках стал предсказуемее: пустой запрос больше не включает режим удаленного поиска.

### Изменения поведения
- Для срабатывания «потяни, чтобы обновить» теперь нужно коротко удержать жест перед отпусканием.
- Во время обновления текущий список остается видимым, пока загружаются новые данные.
- Удаленный поиск включается только при непустом запросе.

### BREAKING CHANGES
- None

### Риски / Что протестировать
- Проверить, что «потяни, чтобы обновить» срабатывает только после осознанного короткого удержания.
- Проверить, что список не мигает в пустое состояние во время обновления.
- Проверить, что при пустом поисковом запросе на удаленных источниках показывается обычный режим просмотра.
- Проверить, что обложки и статусные индикаторы корректно обновляются при прокрутке длинных списков.