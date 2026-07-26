I've reviewed the full input. This release is overwhelmingly refactor/internal, but there are genuine user-facing **fixes** buried in it:

1. **History not saved but shown** → now rolls back if the write fails (no phantom entries reverting on restart) — `PlaybackHistoryRepository`
2. **Bookmarks/labels destroyed on transient read errors** → writes now abort instead of overwriting good data (protects bookmarks/labels) — `StpDbAccess`
3. **Repeated failing history scans** → stops retrying a failing scan every call — `PlaybackHistoryRepository`
4. **Cross-domain download/resume header bug** (blank-domain latent bug + Referer/Origin sanitize parity) — downloads and resume more reliable on certain sources
5. **Help screen crash-safety** → graceful fallback if a help file is missing
6. **Orphaned probe files** in Downloads → bounded to at most one

Everything else (PlaybackAuxController, LibraryArtworkCache, SeekRateLimiter extractions, WhileSubscribed constant, `@Volatile`, WARN logging, integrity.hashes caching) is internal with no user-visible behavior change.

The task's output format differs from the skill's three-block format — the explicit task instructions (the file-driven request) take precedence. I'll produce the requested format.

---

# Release notes — 0.0.74

Release date: 26-Jul-2026

## English
- Fixed a bug where recently played items could appear in your history but silently disappear after restarting the app — history is now only shown once it's safely saved.
- Protected your bookmarks and labels from being erased by a temporary read glitch; the app now refuses to overwrite existing data it can't fully read, instead of replacing it with blanks.
- Stopped the app from repeatedly retrying a failing history scan, which could waste resources in the background.
- Improved reliability of playback and downloads on sources that stream from a separate media host, closing an edge case that could break cross-host downloading and resume.
- The Help screen no longer fails to open if a help page for your language is missing — it falls back gracefully instead.
- Cleaned up how a storage-access check works so it no longer leaves stray hidden files behind in your Downloads folder.
- General stability and maintenance improvements under the hood.

### Behavior changes
- Playback history now updates only after the change is confirmed saved to disk, so what you see always matches what survives a restart.
- If the app can't read your existing saved data during a write, it aborts that write to preserve your bookmarks and position rather than risk losing them.

### BREAKING CHANGES
- None

### Risks / What to test
- Play several books and confirm history entries persist correctly after fully closing and reopening the app.
- Add, edit, and jump to bookmarks; verify none are lost after backgrounding/resuming or switching books.
- Confirm playback position resumes correctly, including on sources that stream from a separate media host.
- Start and complete downloads (including on cross-host sources) and verify they finish and play back.
- Open the Help screen in different device languages and confirm it always loads.
- Check the sleep timer, motion-reset, schedule, and volume fade-out still behave normally.

## Русский

## Русский
- Исправлена ошибка, из-за которой недавно прослушанное могло появляться в истории, но затем незаметно исчезать после перезапуска приложения — история теперь отображается только после надёжного сохранения.
- Защищены ваши закладки и метки от стирания из-за временного сбоя чтения: приложение больше не перезаписывает существующие данные, которые не смогло полностью прочитать, вместо того чтобы заменять их пустыми.
- Приложение больше не повторяет без конца неудавшееся сканирование истории, что могло впустую расходовать ресурсы в фоне.
- Повышена надёжность воспроизведения и загрузок для источников, которые отдают аудио с отдельного медиа-хоста — устранён редкий случай, ломавший загрузку и возобновление между хостами.
- Экран «Справка» больше не перестаёт открываться, если страница справки для вашего языка отсутствует — вместо этого происходит корректный запасной вариант.
- Улучшена проверка доступа к хранилищу: она больше не оставляет лишних скрытых файлов в папке «Загрузки».
- Общие улучшения стабильности и обслуживания «под капотом».

### Изменения в поведении
- История воспроизведения теперь обновляется только после подтверждённого сохранения на диск, поэтому увиденное всегда совпадает с тем, что сохранится после перезапуска.
- Если во время записи приложение не может прочитать ваши уже сохранённые данные, оно отменяет эту запись, чтобы сохранить закладки и позицию, а не рисковать их потерей.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
- Нет

### Риски / Что протестировать
- Прослушайте несколько книг и убедитесь, что записи истории корректно сохраняются после полного закрытия и повторного открытия приложения.
- Добавляйте, редактируйте и переходите к закладкам; проверьте, что ни одна не теряется после сворачивания/возобновления или смены книги.
- Убедитесь, что позиция воспроизведения корректно возобновляется, в том числе на источниках, отдающих аудио с отдельного медиа-хоста.
- Запустите и завершите загрузки (включая межхостовые источники), убедитесь, что они завершаются и воспроизводятся.
- Откройте экран «Справка» на разных языках устройства и убедитесь, что он всегда загружается.
- Проверьте, что таймер сна, сброс по движению, расписание и плавное уменьшение громкости работают как прежде.
