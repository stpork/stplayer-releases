# Release notes — 0.0.31

Release date: 05-Mar-2026 

## English
- Improved YouTube source stability to better handle upstream API/session changes, reducing playback failures.
- Improved playback resolution for videos, playlists, and shorts when primary API calls fail and fallback flows are needed.
- Improved YouTube search and item link generation with template-based URLs and proper query encoding, reducing broken opens from search results.
- Improved consent/session handling across web and mobile domains, which helps with restricted-content and first-load reliability.
- Improved provider loading safety: missing or invalid source configs are now skipped cleanly instead of causing unstable provider behavior.
- Improved RuTracker parsing reliability for topic detection and detail metadata (including size), improving library item completeness.

### Behavior changes
- Providers not present in the bundled source manifest, or missing their config files, are now automatically excluded from active source lists.
- YouTube URL generation now follows configurable templates for watch/playlist/search links.

### BREAKING CHANGES
- None

### Risks / What to test
- Verify YouTube playback for a regular video, a playlist item, and a short.
- Verify YouTube search results open correctly and preserve the intended target.
- Verify provider list loading after app start (no missing/invalid providers shown as active).
- Verify RuTracker detail pages still show expected metadata and downloadable content.

## Русский
- Улучшена стабильность источника YouTube: приложение лучше обрабатывает изменения API/сессий на стороне сервиса, что снижает число сбоев воспроизведения.
- Улучшено получение потоков для видео, плейлистов и Shorts при отказе основного API и переходе на резервные сценарии.
- Улучшено формирование ссылок YouTube для поиска и элементов через шаблоны URL и корректное кодирование запросов, что уменьшает число некорректных открытий из результатов поиска.
- Улучшена обработка consent/session для web и mobile доменов, что повышает надежность первой загрузки и работы с ограниченным контентом.
- Повышена надежность загрузки источников: отсутствующие или некорректные конфиги теперь корректно пропускаются, а не приводят к нестабильной работе источников.
- Улучшена надежность парсинга RuTracker для определения разделов и метаданных карточки (включая размер), что повышает полноту данных в библиотеке.

### Behavior changes
- Источники, которых нет в встроенном манифесте или у которых отсутствуют конфиг-файлы, теперь автоматически исключаются из активного списка.
- Формирование YouTube-ссылок теперь использует настраиваемые шаблоны для watch/playlist/search.

### BREAKING CHANGES
- None

### Risks / What to test
- Проверить воспроизведение YouTube для обычного видео, элемента плейлиста и Shorts.
- Проверить, что результаты поиска YouTube открываются корректно и ведут на нужный контент.
- Проверить загрузку списка источников после запуска приложения (невалидные/отсутствующие источники не должны отображаться как активные).
- Проверить, что на страницах деталей RuTracker по-прежнему отображаются ожидаемые метаданные и доступный для загрузки контент.