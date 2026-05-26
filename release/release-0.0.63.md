# Release notes — 0.0.63

Release date: 27-May-2026

## English
- Swiping between library sources is now reliable. Switching to another source and back no longer leaves swipe navigation stuck or disabled.
- Each source now tracks its own content independently, so a slow or empty source loading in the background can no longer block swiping on the source you're actually viewing.
- Starting a drag on a book cover or list item now correctly hands off to page navigation, so you can swipe between screens without your finger getting "trapped" on the item.
- Faster library and history refresh: folders and saved positions are now read in parallel instead of one at a time, noticeably speeding up scans of large collections.
- Opening a device or shared-storage folder source is faster — the folder tree is now scanned once instead of twice, and large nested folders no longer load one folder at a time.
- Animation timing for spinners and hold-to-act rings is now consistent and predictable across devices, regardless of system animation-speed settings.

### Behavior changes
- Hold-to-act rings and loading spinners now run at a fixed, design-intended speed and are no longer sped up or slowed down by the device's developer animation-scale setting.
- Beginning a swipe gesture on top of an item now releases it for page navigation once you move past a short threshold, instead of being treated only as a tap or long-press.

### BREAKING CHANGES
- None

### Risks / What to test
- Swipe left/right between multiple library sources, including switching away and back; confirm swipe stays responsive.
- Swipe between Library, Player, and Book screens starting the gesture on top of a cover/list item.
- Confirm swipe is gated correctly while a source is still loading or empty, and re-enables once items appear.
- Refresh History and large device/shared-storage folders; verify books, covers, durations, and saved positions are correct and faster.
- Verify hold-to-act (long-press) timing and spinner animations look correct with various device animation-speed settings.

## Русский

### Общее
- Свайп между источниками библиотеки теперь работает надёжно. Переключение на другой источник и обратно больше не оставляет навигацию свайпом «залипшей» или отключённой.
- Каждый источник теперь отслеживает своё содержимое независимо, поэтому медленный или пустой источник, загружающийся в фоне, больше не блокирует свайп в том источнике, который вы сейчас просматриваете.
- Начало жеста перетаскивания на обложке книги или элементе списка теперь корректно передаётся навигации по экранам — палец больше не «застревает» на элементе.
- Ускорено обновление библиотеки и истории: папки и сохранённые позиции теперь читаются параллельно, а не по одной, что заметно ускоряет сканирование больших коллекций.
- Открытие источника-папки с устройства или общего хранилища стало быстрее — дерево папок теперь сканируется один раз вместо двух, а большие вложенные папки больше не загружаются по одной.
- Тайминг анимаций индикаторов загрузки и колец удержания теперь стабилен и предсказуем на всех устройствах, независимо от системных настроек скорости анимации.

### Изменения поведения
- Кольца удержания и индикаторы загрузки теперь работают с фиксированной, задуманной разработчиком скоростью и больше не ускоряются и не замедляются настройкой масштаба анимации в режиме разработчика.
- Начало свайпа поверх элемента теперь передаёт жест навигации по экранам после прохождения небольшого порога, а не трактуется только как нажатие или долгое удержание.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
- Нет

### Риски / Что протестировать
- Свайпайте влево/вправо между несколькими источниками библиотеки, включая переключение туда и обратно; убедитесь, что свайп остаётся отзывчивым.
- Свайпайте между экранами Библиотеки, Плеера и Книги, начиная жест поверх обложки/элемента списка.
- Убедитесь, что свайп корректно блокируется, пока источник ещё загружается или пуст, и снова включается, когда появляются элементы.
- Обновите Историю и большие папки с устройства/общего хранилища; проверьте, что книги, обложки, длительности и сохранённые позиции корректны и загружаются быстрее.
- Проверьте тайминг удержания (долгого нажатия) и анимации индикаторов при разных настройках скорости анимации устройства.
