# Release notes — 0.0.61

Release date: 20-May-2026

## English

### New
- In-app Help screen (Settings → About → Help). Cheatsheet in 12 languages.
- Long-press Pause (2s) → Stop with heavy haptic; book stays on screen with cover and Play button.
- Long-press rewind / fast-forward → ±30 min.
- Long-press previous / next track → jump to 0% / 100% of the book.
- Long-press progress ring indicates hold time.
- YouTube downloads.

### Player
- Global progress bar tracks the whole audiobook, not the current track.
- Pause → Play resumes at the saved position.
- Replay of a finished book starts from 0 on every source and entry path.
- Seek lands at target (was off by up to −30 min on some sources).
- End-of-book seek guard.
- Thin progress bar below controls when minimized; consistent spacing.

### Library & mini-player
- Tapping a book opens the book you tapped (no cross-source preview leak).
- Filled download icons.
- File picker uses a solid 82% black scrim.
- Error toast no longer shows "HTTP Code: 1004" for playback engine errors.

### Stability
- No more crash on rapid torrent switching.
- Cold start no longer engages torrent magnets / DHT.
- Tapping a second torrent book cancels the first immediately (was up to 90 s freeze).
- Bluetooth / headset / lockscreen controls survive book and source switches.
- Library no longer hangs on slow providers (pagination first-page timeout).

### Reliability
- Chrome-shaped TLS handshake (Conscrypt) — fewer silent "403 Forbidden".
- DDoS-Guard / Cloudflare 520-526 retries tuned to observed recovery floors.
- Browser-shape Referer + parallel mirror fan-out on RuTracker-class sources.
- WebView cookie-warmup replaced by a Cloudflare-only detector.
- First magnet on a fresh install resolves: longer metadata timeout + DHT pre-warm.
- Longer cache for content-hashed CDN images.

### Behavior changes
- Play on a finished book always restarts from 0.
- Long-press on Pause → Stop with decorative preview (was: empty screen).
- Cold-start does not auto-engage torrents.

### BREAKING CHANGES
- None.

### Risks / What to test
- Resume from pause mid-book on local / SAF / web / torrent sources.
- Replay a finished book — must restart from 0.
- Double-tap two torrent books — the second supersedes within seconds.
- Long-press Pause for 2 s — heavy haptic, book stays on screen.
- Long-press rewind / forward — 30 min jump.
- Help on each of 12 languages.
- Bluetooth / headset transport after switching sources.
- YouTube playlist download + offline playback.

---

## Русский

### Новое
- Встроенная справка (Настройки → О приложении → Справка). Шпаргалка на 12 языках.
- Long-press Pause (2 с) → Stop с heavy haptic; книга остаётся на экране с обложкой и кнопкой Play.
- Long-press rewind / fast-forward → ±30 минут.
- Long-press previous / next track → к 0% / 100% книги.
- Анимированный круг показывает прогресс long-press.
- Скачивание из YouTube.

### Плеер
- Глобальный скруббер показывает позицию всей аудиокниги, а не текущего трека.
- Pause → Play продолжает с сохранённой позиции.
- Re-play дочитанной книги стартует с 0 на любом источнике и точке входа.
- Seek приземляется куда тапнул (раньше уезжал до −30 минут на части источников).
- End-of-book seek guard.
- Тонкий progress bar под кнопками в minimized режиме, консистентная дистанция.

### Библиотека и мини-плеер
- Тапаешь книгу — открывается она (не утечка preview с другого источника).
- Filled иконки скачивания.
- File picker — solid 82% чёрный scrim.
- Toast ошибок больше не показывает «HTTP Code: 1004» для media3 ошибок.

### Стабильность
- Нет краша при быстром переключении торрент-источников.
- Cold start не запускает торрент-magnet'ы / DHT.
- Тап второй торрент-книги отменяет первую сразу (было до 90 с фриза).
- Bluetooth / гарнитура / lockscreen работают после смены книг и источников.
- Библиотека не зависает на медленных провайдерах (pagination first-page timeout).

### Надёжность
- TLS handshake как у Chrome (Conscrypt) — меньше тихих «403 Forbidden».
- 520-526 ретраи для DDoS-Guard / Cloudflare настроены по наблюдаемым floor'ам восстановления.
- Browser-shape Referer + параллельный fan-out по mirror'ам на RuTracker-источниках.
- WebView cookie-warmup заменён на Cloudflare-детектор.
- Первый magnet на свежей установке резолвится: длиннее metadata timeout + pre-warm DHT.
- Длиннее кэш для content-hashed CDN-картинок.

### Изменения поведения
- Play на дочитанной книге всегда рестартит с 0.
- Long-press на Pause → Stop с decorative preview (было: пустой экран).
- Cold-start не auto-engage'ит торренты.

### BREAKING CHANGES
- Нет.

### Риски / Что протестировать
- Resume из паузы посреди книги на local / SAF / web / torrent.
- Re-play дочитанной книги — рестарт с 0.
- Двойной тап двух торрент-книг — вторая переписывает первую за секунды.
- Long-press Pause 2 с — heavy haptic, книга на экране.
- Long-press rewind / forward — 30-минутный прыжок.
- Справка на 12 языках.
- Bluetooth / гарнитура после переключения источников.
- YouTube плейлист — скачать + offline.
