I have sufficient context now. Here are the release notes:

---

# Release notes — 0.0.72

Release date: 20-Jul-2026

## English

- **Global Search** — a new search tab that queries all your sources at once. Results stream in as each source responds, with matched words highlighted. Filter by Audiobooks, Genres, Authors, or Performers from the top bar. Supports all the same gestures (double-tap, long-press, swipes) as any other list. Open it from the Drawer or from the search button on the Book screen.
- **Maximum playback speed raised to 3.0×** (was 2.0×). Speed is saved per book as before.
- **Pitch control** — adjust pitch ±12 semitones without changing speed, from the top bar on the Player screen.
- **Sleep timer: stop at end of track** — in addition to a fixed duration, you can now set the timer to stop when the current track ends.
- **Sleep timer shake-to-reset** now has three modes: always, only during volume fade, or never.
- **Ratings now appear in book lists** for sources that provide them — you no longer have to open a book detail page to see its score.
- **Book detail page opens faster** — review loading no longer blocks the page from appearing.
- **Better battery use while the screen is off** — background housekeeping tasks pause when the app is in the background and resume when you return.
- **Scraper fixes across multiple sources** — views, ratings, durations, and descriptions now appear more reliably on list cards and detail pages.
- **In-app help updated** in all 12 supported languages, including a new Taps & Gestures reference section and Global Search documentation.

### Behavior changes

- The in-app help Library section now consolidates tap/swipe gestures into a single "Taps & Gestures" reference rather than listing them per screen. Behavior is unchanged.
- Ratings that were previously always hidden on list cards are now shown where available.

### BREAKING CHANGES

None

### Risks / What to test

- Global Search: open from Drawer and from Book screen; verify results load for multiple sources; test swipe-right to Book and Back navigation.
- Playback speed: set to 3.0× and verify audio plays correctly; confirm speed persists after closing and reopening a book.
- Pitch control: adjust up and down; confirm it does not affect speed; confirm it resets independently.
- Sleep timer: set "end of track" mode; verify it stops at the right moment.
- Ratings on list cards: open a source that shows ratings and confirm the score appears without opening the book.
- Background battery: background the app, wait 2+ minutes, return — confirm no extra wake-ups or ANR.

---

## Русский

- **Глобальный поиск** — новая вкладка, которая запрашивает все источники одновременно. Результаты появляются по мере ответа каждого источника, совпавшие слова подсвечиваются. Фильтр в верхней панели: Аудиокниги, Жанры, Авторы, Исполнители. Поддерживаются те же жесты (двойной тап, долгий тап, свайпы), что и в обычных списках. Открыть можно из Drawer или кнопкой поиска на экране Книги.
- **Максимальная скорость воспроизведения увеличена до 3.0×** (было 2.0×). Скорость по-прежнему сохраняется для каждой книги отдельно.
- **Управление тоном** — регулировка тона ±12 полутонов без изменения скорости, в верхней панели экрана Плеера.
- **Таймер сна: остановка по окончании трека** — помимо фиксированной длительности, теперь можно выбрать остановку в конце текущего трека.
- **Сброс таймера сна встряхиванием** теперь настраивается: всегда, только во время затихания, или никогда.
- **Рейтинги теперь видны в списке книг** для источников, которые их предоставляют — открывать страницу книги для этого больше не нужно.
- **Страница книги открывается быстрее** — загрузка отзывов больше не блокирует появление страницы.
- **Меньше расхода батареи при выключенном экране** — фоновые задачи приостанавливаются, когда приложение свёрнуто, и возобновляются при возврате.
- **Исправления скраперов для нескольких источников** — просмотры, рейтинги, длительность и описания теперь стабильнее отображаются на карточках и страницах книг.
- **Встроенная справка обновлена** на всех 12 поддерживаемых языках: добавлен раздел «Тапы и жесты» и документация по глобальному поиску.

### Изменения поведения

- Раздел «Библиотека» в справке теперь объединяет описание жестов в единый раздел «Тапы и жесты» вместо их перечисления на каждом экране. Само поведение не изменилось.
- Рейтинги, которые ранее скрывались в карточках списка, теперь отображаются там, где источник их предоставляет.

### Критические изменения

Отсутствуют

### Риски / Что проверить

- Глобальный поиск: открытие из Drawer и с экрана Книги; загрузка результатов из нескольких источников; свайп вправо на Книгу и навигация «Назад».
- Скорость воспроизведения: установить 3.0×, убедиться в корректном воспроизведении; проверить сохранение после закрытия и повторного открытия книги.
- Управление тоном: изменить вверх и вниз; убедиться, что скорость не меняется; проверить независимый сброс.
- Таймер сна: режим «конец трека»; убедиться в остановке в нужный момент.
- Рейтинги в карточках: открыть источник с рейтингами и проверить отображение оценки без входа в книгу.
- Фоновая батарея: свернуть приложение, подождать 2+ минуты, вернуться — убедиться в отсутствии лишних пробуждений или ANR.
