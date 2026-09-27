# Release notes — 0.0.90

Release date: 27-Sep-2026

## English

- Global search now loads more books, authors, narrators and genres as you scroll.
- Improved catalog sorting and page loading across several online sources.
- Fixed lists stopping too early when a page contains fewer results than expected.
- Kept list order stable during refreshes and prevented saved settings from overriding a newly selected list or sort order.
- Fixed interrupted search results getting stuck when returning from an author, narrator or genre’s books.
- Improved global search reliability when some sources respond more slowly than others.

### Behavior changes

- If a search source fails, use **Retry** to continue from its unfinished page while keeping results already loaded.

### BREAKING CHANGES

None

### Risks / What to test

- Check sorting, refreshing and scrolling through multiple pages in your usual sources.
- Test global search by book, author, narrator and genre, including opening results and going back.
- After a connection failure, check that **Retry** loads missing results without clearing existing ones.
- Check scrolling and remote-control focus on TV.

## Русский

- Глобальный поиск теперь подгружает больше книг, авторов, исполнителей и жанров при прокрутке.
- Улучшены сортировка каталогов и загрузка следующих страниц в нескольких онлайн-источниках.
- Исправлено преждевременное завершение списка, если на странице оказалось меньше результатов, чем ожидалось.
- Порядок элементов при обновлении стал стабильнее, а сохранённые настройки больше не отменяют только что выбранный список или сортировку.
- Исправлено зависание подгрузки результатов поиска при возврате из списка книг автора, исполнителя или жанра.
- Глобальный поиск стал надёжнее, когда одни источники отвечают медленнее других.

### Изменения в работе приложения

- Если поиск в источнике завершился ошибкой, нажмите **Повторить**, чтобы продолжить с незагруженной страницы, сохранив уже полученные результаты.

### НЕСОВМЕСТИМЫЕ ИЗМЕНЕНИЯ

Нет

### Риски / Что проверить

- Проверьте сортировку, обновление и прокрутку нескольких страниц в привычных источниках.
- Проверьте глобальный поиск по книгам, авторам, исполнителям и жанрам, включая открытие результатов и возврат назад.
- После сбоя соединения проверьте, что кнопка **Повторить** загружает недостающие результаты, не очищая уже показанные.
- Проверьте прокрутку и перемещение фокуса с пульта на телевизоре.