# Release notes — 0.0.26

Release date: 25-Feb-2026 

## English
- Improved double-tap-to-play reliability in Library, History, and Favorites, especially right after scrolling.
- Expanded the double-tap detection window, making playback start more reliable when taps are slightly slower.
- Empty-state pages are now scrollable, so guidance text and actions stay accessible on smaller screens or with larger text sizes.
- Improved media-session callback handling for better stability during service lifecycle transitions (including external browsing/control clients).

### Behavior changes
- In **Double tap** playback mode, post-scroll tap filtering is no longer applied, so double taps are accepted immediately after scrolling.
- The double-tap timeout is now longer (more forgiving) than before.
- Empty states in main list views now support vertical scrolling.

### BREAKING CHANGES
- None

### Risks / What to test
- Verify single-tap mode still blocks accidental playback after list scrolling.
- Verify double-tap mode starts playback reliably in Library, History, and Favorites (including immediately after scrolling).
- Verify empty-state screens remain readable and scroll correctly on small displays and large-font accessibility settings.
- Verify media browsing/controls remain stable when app/service is started, backgrounded, and stopped.

## Русский
- Улучшена надежность запуска по двойному нажатию в Библиотеке, Истории и Избранном, особенно сразу после прокрутки.
- Увеличено окно распознавания двойного нажатия, поэтому запуск воспроизведения стал надежнее при немного более медленных нажатиях.
- Экраны пустого состояния теперь прокручиваются, поэтому текст подсказок и действия остаются доступными на маленьких экранах и при увеличенном размере шрифта.
- Улучшена обработка колбэков медиасессии для более стабильной работы при переходах жизненного цикла сервиса (включая внешние клиенты просмотра/управления).

### Behavior changes
- В режиме запуска воспроизведения **Double tap** фильтрация нажатий после прокрутки больше не применяется, поэтому двойные нажатия принимаются сразу после скролла.
- Таймаут двойного нажатия теперь длиннее (более терпимый), чем раньше.
- Пустые состояния в основных списках теперь поддерживают вертикальную прокрутку.

### BREAKING CHANGES
- None

### Risks / What to test
- Проверить, что режим single tap по-прежнему защищает от случайного запуска после прокрутки списка.
- Проверить, что в режиме double tap воспроизведение стабильно запускается в Библиотеке, Истории и Избранном (в том числе сразу после скролла).
- Проверить, что экраны пустого состояния корректно читаются и прокручиваются на маленьких дисплеях и при увеличенных шрифтах.
- Проверить стабильность просмотра медиатеки и управления при запуске, сворачивании в фон и остановке приложения/сервиса.