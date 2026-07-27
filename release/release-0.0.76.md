I've analyzed the full changelog. The only user-visible change in 0.0.76 is the fix for one audiobook source that migrated to HLS streaming. Everything else is CI setup, dependency bumps, docs, test de-flaking, and internal cleanup — none of which is user-facing.

Per the rules (no source codes, consolidate, only user-visible value), here are the release notes:

# Release notes — 0.0.76

Release date: 28-Jul-2026

## English
- Fixed playback on an online source that recently switched its audiobooks to adaptive HLS streaming — titles that had stopped playing with a "no track" error now load and play correctly again.
- General reliability and stability improvements under the hood.

### Behavior changes
- None visible in day-to-day use, beyond restored playback on the affected source.

### BREAKING CHANGES
- None

### Risks / What to test
- Browse and play a few audiobooks from the affected online source; confirm tracks load and play without a "no track" error.
- Verify seeking, chapter/track switching, and resume-from-position work on those streamed titles.
- Confirm playback on other online sources and local files is unaffected.

## Русский

## Примечания к выпуску — 0.0.76

Дата выпуска: 28-июл-2026

- Исправлено воспроизведение на одном онлайн-источнике, который недавно перевёл аудиокниги на адаптивную потоковую передачу HLS: книги, которые переставали воспроизводиться с ошибкой «нет дорожки», снова корректно загружаются и играют.
- Общие улучшения надёжности и стабильности под капотом.

### Изменения в поведении
- В повседневном использовании заметных изменений нет, кроме восстановленного воспроизведения на затронутом источнике.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
- Нет

### Риски / Что протестировать
- Откройте и воспроизведите несколько аудиокниг с затронутого онлайн-источника; убедитесь, что дорожки загружаются и играют без ошибки «нет дорожки».
- Проверьте перемотку, переключение глав/дорожек и продолжение с сохранённой позиции на этих потоковых книгах.
- Убедитесь, что воспроизведение с других онлайн-источников и локальных файлов не затронуто.
