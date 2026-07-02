# Release notes — 0.0.68

Release date: 02-Jul-2026

## English

- Playback speed range extended to **3.0×** (was 2.0×).
- **Download badges** now appear on the book artwork screen, showing download progress, completion, and failure states at a glance.
- Pulling to refresh the Downloads list now **reconciles badge states** in a single pass, so artwork icons reflect the true on-disk state immediately.
- Books that are only partially downloaded no longer show a green "completed" checkmark.
- Playback **speed and pitch settings are now preserved** across force-kills and app restarts.
- Fixed a bug where speed changes were saved at the wrong moment, causing the wrong speed to be restored on next launch.
- Downloading ZIP-based audiobooks is now more reliable: the app verifies the archive before marking it complete, retries on transient storage errors, and handles archives with non-standard footers.
- Fixed a failure where a corrupt or missing history file could silently wipe playback progress on reboot; the file is now protected by an atomic write and a fallback recovery path.
- Legacy favorites data is now **migrated** rather than deleted on upgrade — no favorites will be lost.
- Fixed an edge case where the total duration shown for multi-track books was calculated incorrectly.
- Fixed a media notification that could go stale or disappear after asynchronous artwork loading.
- App startup is faster and uses less memory: the torrent networking stack now initializes only when you actually open a torrent source, not on every cold start.
- Help content updated and corrected across all 12 supported languages.
- Settings screen reorganized: download folder and library location are now separate, clearly labeled items.

### Behavior changes

- The torrent source no longer starts background network activity until you navigate to it for the first time in a session.
- The Settings menu labels for backup/restore, ignore lists, mini-player size, and haptic feedback have been renamed to match the actual in-app behavior.

### BREAKING CHANGES

None

### Risks / What to test

- Verify playback speed is restored correctly after a force-kill at each speed setting.
- Download a ZIP-based audiobook end-to-end; confirm the completed badge appears and playback works from the downloaded file.
- Pull-to-refresh on the Downloads screen; confirm badge states match actual on-disk status.
- Open a torrent source from a fresh cold start; confirm DHT bootstraps in the background without impacting app launch time.
- Confirm no favorites are lost after upgrading from 0.0.67.
- Check that partially downloaded books do not show a green completed checkmark.

---

## Русский

- Диапазон скорости воспроизведения расширен до **3.0×** (ранее было 2.0×).
- **Значки загрузки** теперь отображаются прямо на экране обложки книги — показывают прогресс, завершение и ошибки загрузки с первого взгляда.
- Потягивание для обновления на экране загрузок теперь **синхронизирует состояния значков** за один проход, и иконки на обложках сразу отражают реальное состояние файлов.
- Частично загруженные книги больше не отображают зелёную галочку «завершено».
- **Скорость и тон воспроизведения теперь сохраняются** после принудительного завершения приложения и перезапуска.
- Исправлена ошибка, при которой скорость сохранялась в неправильный момент, из-за чего при следующем запуске восстанавливалось неверное значение.
- Загрузка ZIP-аудиокниг стала надёжнее: приложение проверяет архив перед отметкой завершения, повторяет попытку при временных ошибках хранилища и корректно обрабатывает архивы с нестандартным окончанием.
- Исправлена ошибка, при которой повреждённый или отсутствующий файл истории мог незаметно сбрасывать позицию воспроизведения при перезагрузке; файл теперь защищён атомарной записью и путём восстановления.
- Устаревшие данные избранного теперь **мигрируются**, а не удаляются при обновлении — избранное не будет потеряно.
- Исправлен случай неверного подсчёта общей длительности для книг с несколькими дорожками.
- Исправлено уведомление о воспроизведении, которое могло устаревать или исчезать после асинхронной загрузки обложки.
- Приложение запускается быстрее и потребляет меньше памяти: сетевой стек торрентов теперь инициализируется только при первом открытии источника-торрента, а не при каждом холодном старте.
- Справочное содержимое обновлено и исправлено для всех 12 поддерживаемых языков.
- Экран настроек реорганизован: папка загрузок и расположение библиотеки теперь вынесены в отдельные, чётко подписанные пункты.

### Изменения в поведении

- Источник-торрент больше не запускает фоновую сетевую активность до тех пор, пока вы не перейдёте к нему в текущей сессии.
- Метки в меню настроек для резервного копирования/восстановления, чёрных списков, размера мини-плеера и тактильной обратной связи переименованы в соответствии с реальным поведением в приложении.

### Критические изменения

Отсутствуют

### Риски / Что тестировать

- Убедиться, что скорость воспроизведения корректно восстанавливается после принудительного завершения при каждом значении скорости.
- Загрузить ZIP-аудиокнигу от начала до конца; убедиться, что значок завершения появляется и воспроизведение из загруженного файла работает.
- Потянуть для обновления на экране загрузок; убедиться, что состояния значков соответствуют реальному состоянию файлов на диске.
- Открыть источник-торрент после холодного старта; убедиться, что DHT-бутстрап происходит в фоне без влияния на время запуска приложения.
- Убедиться, что избранное не потеряно после обновления с 0.0.67.
- Убедиться, что частично загруженные книги не отображают зелёную галочку завершения.
