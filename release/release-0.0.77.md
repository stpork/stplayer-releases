I have enough signal now. The remaining lines are more help-file translations (repeated across locales) plus source JSON and Kotlin diffs already summarized by the commit messages. The commit list is comprehensive and clear. Let me synthesize the user-facing release notes.

Key user-facing themes from the commits:
- **Android TV support** (new): installable, D-pad navigation across all screens, remote/mouse, help section
- **Landscape two-pane Player and Book layouts**
- **Cloudflare/Turnstile challenge solver** via in-app WebView captcha panel (fixes access to a blocked source)
- **Android Auto improvements**: covers in browse, search via global search with result counts, artwork on results
- **Cover/artwork quality**: sharper Player covers, covers served to Auto/Bluetooth, notification cover
- **Bug fixes**: playback position/history reliability, loading spinner ownership, long-press surviving OEM cancel, playlist indirection not treated as track, pagination fixes
- **Help rewritten** in clean prose + 12 locales, new Taps & Gestures / Android TV sections
- Behavior: single vs double tap wording, back navigation

# Release notes — 0.0.77

Release date: 02-Aug-2026

## English
- **Android TV support**: the app now installs on Android TV and is fully operable with the remote's D-pad or a connected mouse — browse the library, open books, and control playback, with a focus border showing where you are.
- **Landscape two-pane layouts**: the Player and Book screens now use a side-by-side layout in landscape, with sharper cover art and a mini-player-aware bottom edge.
- **Access to challenge-protected sources**: when a source shows a "prove you're human" check, an in-app panel now lets you solve it and continue browsing and playing.
- **Better Android Auto & Bluetooth**: audiobook covers now appear when browsing in the car, search works across all your sources and tells you how many results it found, and results show their artwork.
- **Sharper, more reliable cover art**: covers are crisper on the Player screen, show correctly in the car and on Bluetooth displays, and appear on the playback notification.
- **Sturdier playback position & history**: your position and listening history save more reliably, closing rare cases where a recent position could be lost.
- **Long-press works more reliably**: long-press actions no longer get interrupted on some Samsung and other devices.
- **Playlist fix**: books delivered via a playlist file now load correctly instead of failing.
- **Smoother lists**: fixed a loading spinner that could linger, and improved paging through long result lists.
- **Rewritten Help**: the in-app Help is clearer, with new "Taps & Gestures" and "Android TV" sections, in all 12 languages.

### Behavior changes
- Tap-to-play now respects your chosen tap mode consistently across the catalog, local search, and global search (single or double tap).
- Back navigation retraces your exact path (Player → Book → Search → category) and ends at your source's library.
- Genre, author, and performer cards in global search only open books — they never start playback.
- Sleep timer's "reset when you pick up the phone" is now a single option covering its modes.

### BREAKING CHANGES
- None

### Risks / What to test
- Android TV: install and navigate the library, book, and player entirely by remote; verify focus highlight, hold-Left/Right, OK to play, and chapter switching.
- Landscape: rotate on the Player and Book screens; check cover sharpness and that controls aren't clipped by the mini-player.
- Challenge-protected sources: trigger the human-check panel, solve it, and confirm browsing/playback resumes.
- Android Auto & Bluetooth: browse with covers, run a search, and confirm result counts and artwork; check the notification cover.
- Playback position/history: play, background, and reopen; confirm the last position and history are intact.
- Long-press: verify the long-press menu opens on affected devices.
- Playlist-based books: open and play a book delivered via a playlist file.

## Русский

## Примечания к выпуску — 0.0.77

Дата выпуска: 02-авг-2026

### English → Русский
- **Поддержка Android TV**: приложение теперь устанавливается на Android TV и полностью управляется пультом (крестовиной D-pad) или подключённой мышью — просмотр библиотеки, открытие книг и управление воспроизведением, с рамкой фокуса, показывающей текущее положение.
- **Двухпанельный ландшафтный режим**: экраны «Плеер» и «Книга» в альбомной ориентации теперь используют раскладку бок о бок, с более чёткими обложками и учётом мини-плеера снизу.
- **Доступ к источникам с проверкой**: когда источник показывает проверку «докажите, что вы человек», встроенная панель позволяет пройти её и продолжить просмотр и воспроизведение.
- **Улучшения Android Auto и Bluetooth**: обложки книг теперь отображаются при просмотре в машине, поиск работает по всем источникам сразу и сообщает число найденных результатов, а у результатов показываются обложки.
- **Более чёткие и надёжные обложки**: обложки чётче на экране «Плеер», корректно показываются в машине и на дисплеях Bluetooth, а также появляются в уведомлении воспроизведения.
- **Надёжнее позиция и история воспроизведения**: позиция и история прослушивания сохраняются надёжнее, устранены редкие случаи потери недавней позиции.
- **Надёжнее долгое нажатие**: действия по долгому нажатию больше не прерываются на некоторых устройствах Samsung и других.
- **Исправление плейлистов**: книги, поставляемые через файл-плейлист, теперь загружаются корректно, а не с ошибкой.
- **Более плавные списки**: исправлен индикатор загрузки, который мог задерживаться, и улучшена подгрузка длинных списков результатов.
- **Переписанная справка**: встроенная справка стала понятнее, с новыми разделами «Касания и жесты» и «Android TV», на всех 12 языках.

### Изменения в поведении
- Запуск воспроизведения касанием теперь единообразно учитывает выбранный режим касания в каталоге, локальном и глобальном поиске (одно или двойное касание).
- Кнопка «Назад» проходит по вашему точному пути (Плеер → Книга → Поиск → категория) и заканчивается на библиотеке вашего источника.
- Карточки жанров, авторов и исполнителей в глобальном поиске только открывают книги — они никогда не запускают воспроизведение.
- Опция таймера сна «сброс, когда берёшь телефон в руки» теперь единая настройка, охватывающая её режимы.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
- Нет

### Риски / Что проверить
- Android TV: установите и пройдите по библиотеке, книге и плееру целиком с пульта; проверьте подсветку фокуса, удержание Влево/Вправо, OK для воспроизведения и переключение глав.
- Ландшафт: поверните экраны «Плеер» и «Книга»; проверьте чёткость обложек и что элементы управления не перекрыты мини-плеером.
- Источники с проверкой: вызовите панель проверки на человека, пройдите её и убедитесь, что просмотр/воспроизведение возобновляются.
- Android Auto и Bluetooth: просмотр с обложками, выполните поиск и проверьте число результатов и обложки; проверьте обложку в уведомлении.
- Позиция/история воспроизведения: воспроизведите, сверните и снова откройте; убедитесь, что последняя позиция и история сохранились.
- Долгое нажатие: проверьте, что меню по долгому нажатию открывается на затронутых устройствах.
- Книги на основе плейлистов: откройте и воспроизведите книгу, поставляемую через файл-плейлист.
