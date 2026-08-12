I have everything I need. The user's explicit output format overrides the skill's Google Play/RuStore format. Let me map the changes to user-facing value:

1. **Search finds more books** — global search now keeps provider-relevant results (matches in author/description, not just title) instead of dropping them, ranking weaker matches as "similar"; per-source result cap raised 25→50 (less silent truncation).
2. **Empty search shows "nothing found" not error** — API-catalog sources that return 404 on no-match queries now show empty results instead of a source failure.
3. **Genre search fix** for one source (hits real genre endpoint).
4. **Speed/pitch dial no longer snaps back to 1.00x** mid-adjustment.
5. **Torrent playback recovers from stalls** — read-starvation errors (code 2000) now retry instead of stopping playback terminally.

The rest is tests/docs/version — excluded.

# Release notes — 0.0.80

Release date: 12-Aug-2026

## English
- Global search now shows more relevant results: books that match in the author or description — not just the title — are kept instead of being silently dropped, with weaker matches grouped as "similar" at the bottom of the list.
- Each source can now return up to twice as many search results, so fewer matches are cut off when a source has many hits.
- Searches that genuinely have no matches now clearly show "nothing found" instead of reporting the source as failed.
- Genre search on one catalogue now queries the correct genre listing, returning proper results instead of coming up empty.
- The playback speed and pitch dials no longer jump back to 1.00× while you are still adjusting them.
- Streaming playback now rides out short network stalls and resumes automatically instead of stopping with an error; playback only gives up when the source is genuinely unavailable.

### Behavior changes
- A search with no results is treated as an empty result, not a source error — the source no longer appears "failed" for zero-hit queries.
- Non-title matches still appear in results but are ranked lower, under a "similar" grouping.

### BREAKING CHANGES
- None

### Risks / What to test
- Run global searches where the match is in the author/description but not the title — confirm the book still appears and is ranked as "similar".
- Search a term with no matches — confirm it shows "nothing found", not a source error.
- Search sources with many results — confirm more results show and check for truncation.
- Open the speed and pitch dials, adjust slowly, and confirm the value does not snap back to 1.00×; confirm dismiss-without-apply still restores the prior value.
- Play a stream and interrupt the network briefly — confirm playback recovers instead of stopping; confirm a truly unavailable source still surfaces an error.

## Русский
- Глобальный поиск теперь показывает больше релевантных результатов: книги, совпавшие по автору или описанию, а не только по названию, больше не отбрасываются — менее точные совпадения группируются как «похожие» внизу списка.
- Каждый источник теперь может вернуть вдвое больше результатов поиска, поэтому при большом числе совпадений меньше вариантов обрезается.
- Поиск, у которого действительно нет совпадений, теперь чётко показывает «ничего не найдено», а не сообщает об ошибке источника.
- Поиск по жанру в одном каталоге теперь обращается к правильному разделу жанров и возвращает результаты вместо пустого списка.
- Регуляторы скорости и высоты тона больше не сбрасываются на 1.00× во время настройки.
- Потоковое воспроизведение теперь переживает короткие сбои сети и возобновляется автоматически, а не останавливается с ошибкой; воспроизведение прекращается только если источник действительно недоступен.

### Изменения поведения
- Поиск без результатов трактуется как пустой результат, а не ошибка источника — источник больше не выглядит «сбойным» при запросах без совпадений.
- Совпадения не по названию всё ещё отображаются, но ранжируются ниже, в группе «похожие».

### BREAKING CHANGES
- Нет

### Риски / Что проверить
- Выполните поиск, где совпадение в авторе/описании, но не в названии — убедитесь, что книга остаётся в результатах и помечена как «похожая».
- Поищите запрос без совпадений — убедитесь, что показано «ничего не найдено», а не ошибка источника.
- Поищите в источниках с большим числом результатов — убедитесь, что показывается больше вариантов, проверьте обрезание.
- Откройте регуляторы скорости и тона, медленно поменяйте значение — убедитесь, что оно не сбрасывается на 1.00×; проверьте, что закрытие без применения возвращает прежнее значение.
- Запустите поток и кратко прервите сеть — убедитесь, что воспроизведение восстанавливается, а не останавливается; проверьте, что действительно недоступный источник по-прежнему выдаёт ошибку.
