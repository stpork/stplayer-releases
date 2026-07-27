# Release notes — 0.0.75

Release date: 27-Jul-2026

## English

- **Accidental swipe-to-delete fixed** — removing a book from History or Favorites now requires a deliberate swipe across 80% of the screen width. Previously, a short back-gesture or keyboard-dismiss swipe could silently delete a book.
- **Favorites now reports save failures** — if a favorite could not be written to disk, the star reverts immediately instead of showing success and then losing the change on the next app restart.
- **Favorites and History survive app cancellations** — background operations that are cancelled (e.g., when leaving the app) no longer incorrectly mark the data scan as failed, which previously caused History to appear empty until a manual refresh.
- **Search tab can now be reordered and hidden** — in Manage Sources, the Search tab behaves like any other tab: you can drag it to a different position or toggle its visibility. Previously it was pinned and always shown first.
- **Book tracks preserved when a detail page returns empty** — if fetching a book's detail page yields no tracks (e.g., due to a slow or rate-limited response), the tracks already loaded from the list are kept. Previously this could blank out tracks and make a book unplayable.
- **Navigation Back is more reliable** — the Back button and the swipe-back gesture now share a single consistent algorithm, eliminating edge cases where the previous screen was not restored correctly.
- **Language categories navigate correctly** — browsing by language (where available) now behaves the same as browsing by genre, author, or performer.

### Behavior changes

- The Search tab in Manage Sources can now be reordered and hidden, matching the behavior of all other tabs. Existing installations keep their current tab order unchanged until the user moves Search manually.
- Swipe-to-delete in History and Favorites requires a longer swipe (80% of screen width, up from 50%).

### BREAKING CHANGES

None

### Risks / What to test

- Swipe a book card partway in History and Favorites — confirm it snaps back without deleting at short swipe distances.
- Add and remove a Favorite; confirm the star icon matches the actual saved state after killing and relaunching the app.
- Open Manage Sources; confirm Search appears, can be toggled, and can be dragged to a new position.
- Browse a source by language/genre/author; confirm the Back button returns to the category list correctly.
- Open a book that loaded from the list view; confirm tracks are present on the detail screen.
- Use Back button and swipe-back gesture from several nested screens; confirm the correct previous screen is restored each time.

---

## Русский

- **Исправлено случайное удаление свайпом** — удаление книги из Истории или Избранного теперь требует намеренного свайпа на 80% ширины экрана. Раньше короткий жест «назад» или закрытие клавиатуры могли незаметно удалить книгу.
- **Избранное теперь сообщает об ошибках сохранения** — если отметку не удалось записать на диск, звёздочка сразу же сбрасывается, а не показывает успех и теряет изменение при следующем запуске.
- **Избранное и История не пропадают при отмене фоновых операций** — фоновые задачи, прерванные при выходе из приложения, больше не помечают сканирование данных как неудачное, из-за чего История ранее могла оказаться пустой до ручного обновления.
- **Вкладку Поиск теперь можно перемещать и скрывать** — в разделе «Управление источниками» вкладка Поиск ведёт себя как любая другая: её можно перетащить на другое место или скрыть. Раньше она была закреплена и всегда отображалась первой.
- **Треки книги сохраняются при пустом ответе страницы деталей** — если при загрузке подробной информации о книге треки не вернулись (например, из-за медленного или заблокированного ответа), уже загруженные из списка треки остаются. Раньше это могло обнулять треки и делать книгу недоступной для воспроизведения.
- **Кнопка «Назад» стала надёжнее** — кнопка «Назад» и жест свайпа-назад теперь используют единый алгоритм, что устраняет ситуации, когда предыдущий экран восстанавливался некорректно.
- **Категории по языку работают правильно** — навигация по языкам (там, где она доступна) теперь работает так же, как навигация по жанрам, авторам или исполнителям.

### Изменения поведения

- Вкладку Поиск в разделе «Управление источниками» теперь можно перемещать и скрывать, как любую другую вкладку. У существующих установок порядок вкладок не изменится до тех пор, пока пользователь не переместит Поиск вручную.
- Свайп для удаления в Истории и Избранном теперь требует более длинного жеста (80% ширины экрана вместо 50%).

### Критические изменения

Отсутствуют

### Риски / Что проверить

- Сделать короткий свайп по карточке книги в Истории и Избранном — убедиться, что карточка возвращается на место без удаления.
- Добавить и удалить книгу из Избранного; убедиться, что состояние звёздочки соответствует реально сохранённым данным после перезапуска приложения.
- Открыть «Управление источниками»; убедиться, что Поиск отображается, его можно включить/выключить и перетащить на новое место.
- Просмотреть источник по языку/жанру/автору; убедиться, что кнопка «Назад» корректно возвращает к списку категорий.
- Открыть книгу, загруженную из списка; убедиться, что треки отображаются на экране деталей.
- Использовать кнопку «Назад» и жест свайпа с нескольких вложенных экранов; убедиться, что каждый раз восстанавливается правильный предыдущий экран.
