# Release notes — 0.0.88

Release date: 17-Sep-2026

## English

- Improved scheduled sleep timers, with more predictable countdowns when you resume listening.
- Fixed bookmark edits potentially overwriting newer listening progress or book details.
- Protected synced bookmarks from accidental deletion when some library data cannot be read.
- Fixed loading further search results when a catalogue uses the default search.
- Restored history clearing on Android TV and improved protection against accidental menu activation.
- Made physical remote playback controls consistent across screens.
- Improved privacy during streaming and downloads by restricting cookie sharing when a connection redirects to another site.

### Behavior changes

- The default sleep timer schedule now runs from 22:00 to 10:00 the next morning. When the timer expires within that window, its selection is retained. Pressing Play starts a fresh countdown only if you are still within the window; otherwise, the timer switches off. Playback never restarts automatically.
- Cancelling a scheduled sleep timer keeps it from automatically activating again during the same schedule window.
- On physical remote controls, briefly pressing and releasing Next/Previous changes chapters; holding either button seeks by the configured interval. Holding the on-screen Next button still jumps to the end of the book.
- Sync stops if it cannot read all required library data, protecting previously synced bookmarks.

### BREAKING CHANGES

None

### Risks / What to test

- Check sleep timer expiry, cancellation and manual playback restart inside and outside the schedule window.
- Edit bookmarks while listening, reopen the book and verify that progress and book details are preserved.
- Check sync with temporarily inaccessible books and confirm that bookmarks remain intact.
- On Android TV, test history clearing, menu activation and short and long presses of remote media buttons.
- Check later pages of search results, streaming and downloads from your usual sources.

## Русский

- Улучшена работа таймера сна по расписанию: отсчёт при возобновлении прослушивания стал предсказуемее.
- Исправлена ошибка, из-за которой редактирование закладок могло перезаписать более свежую позицию прослушивания или сведения о книге.
- Синхронизированные закладки защищены от случайного удаления, если часть данных библиотеки не удаётся прочитать.
- Исправлена загрузка следующих страниц результатов в каталогах, использующих общий поиск.
- Восстановлена очистка истории на Android TV и улучшена защита от случайного выбора действий в меню.
- Физические медиакнопки пульта теперь одинаково управляют воспроизведением на разных экранах.
- Улучшена защита конфиденциальности при прослушивании онлайн и скачивании: передача cookie при перенаправлении на другой сайт ограничена.

### Изменения в поведении

- Стандартный интервал таймера сна по расписанию теперь длится с 22:00 до 10:00 следующего утра. Если таймер срабатывает в этом интервале, выбранная настройка сохраняется. Нажатие «Воспроизвести» запускает новый отсчёт, только если текущее время всё ещё входит в интервал; иначе таймер выключается. Воспроизведение автоматически не возобновляется.
- После отмены таймер сна по расписанию больше не включается автоматически в том же интервале.
- Короткое нажатие и отпускание физических кнопок «Следующая/Предыдущая» на пульте переключает главы; удержание перематывает на заданный интервал. Удержание экранной кнопки «Следующая» по-прежнему переводит в конец книги.
- Синхронизация останавливается, если не удаётся прочитать все необходимые данные библиотеки, сохраняя ранее синхронизированные закладки.

### НЕСОВМЕСТИМЫЕ ИЗМЕНЕНИЯ

Нет

### Риски / Что проверить

- Проверьте срабатывание и отмену таймера сна, а также ручное возобновление воспроизведения внутри и вне интервала расписания.
- Измените закладки во время прослушивания, снова откройте книгу и убедитесь, что позиция и сведения о книге сохранились.
- Проверьте синхронизацию при временно недоступных книгах и убедитесь, что закладки не потерялись.
- На Android TV проверьте очистку истории, выбор действий в меню, короткие и долгие нажатия медиакнопок пульта.
- Проверьте следующие страницы результатов поиска, прослушивание онлайн и скачивание из привычных источников.