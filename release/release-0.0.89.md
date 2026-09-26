# Release notes — 0.0.89

Release date: 27-Sep-2026

## English

- Online playback recovers more reliably from temporary connection failures while preserving your listening position.
- Improved recovery when a source’s playback links expire.
- Safer download resume helps prevent incomplete or mismatched audio from being saved.
- Improved loading of book descriptions and reviews where supported by the source.
- Review loading failures are now distinguished from an empty review list, and previously loaded reviews remain visible if a later page fails.
- Updated the in-app guide with advice on network interruptions, download resume and loading book details.

### Behavior changes

- Online playback automatically retries temporary connection failures and may wait for data. Pause or stop to prevent playback from continuing when connectivity returns.
- If a source file has changed or a saved partial download cannot be verified, the affected track downloads again from the beginning.
- Descriptions and reviews may finish loading after you open a book. Reopen the book to retry a failed review load.

### BREAKING CHANGES

None

### Risks / What to test

- Check playback recovery after losing and restoring connectivity, including in the background.
- Confirm that pause and stop prevent playback from restarting when connectivity returns.
- Interrupt and resume downloads; check that completed tracks play correctly offline.
- Check descriptions and reviews, including retrying failed loads and keeping existing reviews visible when a later page fails.

## Русский

- Онлайн-воспроизведение надёжнее восстанавливается после временных сбоев связи с сохранением позиции прослушивания.
- Улучшено восстановление воспроизведения, когда срок действия ссылок источника истекает.
- Более безопасное возобновление скачивания помогает избежать сохранения неполных аудиофайлов или файлов с несовпадающими частями.
- Улучшена загрузка описаний книг и отзывов, если источник их предоставляет.
- Ошибка загрузки отзывов теперь отличается от пустого списка, а уже загруженные отзывы остаются видны при сбое загрузки следующей страницы.
- Встроенная справка дополнена рекомендациями о перебоях связи, возобновлении скачивания и загрузке сведений о книге.

### Изменения в поведении

- При временных сбоях связи онлайн-плеер автоматически повторяет попытки и может ожидать данные. Нажмите паузу или остановку, если не хотите продолжать прослушивание после восстановления связи.
- Если файл у источника изменился или сохранённую часть загрузки нельзя проверить, соответствующий трек скачивается заново с начала.
- Описания и отзывы могут догружаться после открытия книги. Чтобы повторить неудавшуюся загрузку отзывов, откройте книгу заново.

### НЕСОВМЕСТИМЫЕ ИЗМЕНЕНИЯ

Нет

### Риски / Что проверить

- Проверьте восстановление воспроизведения после потери и возвращения связи, в том числе в фоновом режиме.
- Убедитесь, что после паузы или остановки воспроизведение не запускается само при восстановлении связи.
- Прервите и возобновите скачивание; проверьте воспроизведение скачанных треков без интернета.
- Проверьте описания и отзывы, включая повторную загрузку после ошибки и сохранение уже показанных отзывов при сбое загрузки следующей страницы.