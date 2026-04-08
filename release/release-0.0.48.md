
# Release notes — 0.0.48

Release date: 06-Apr-2026

## English

- **Restored library scroll positions**: Grid scroll positions now persist correctly across app restarts, so you return to where you left off.
- **No more empty screen after background**: Memory pressure handling no longer clears your loaded library items, so the app shows your books immediately when you return.
- **Improved sleep timer behavior**: The fade-out during sleep timer now uses a linear volume curve for more consistent perceived volume decrease.
- **Refreshed haptic feedback**: Button press vibrations use a new pattern for clearer tactile response.
- **Reduced CPU usage**: Slower progress indicator animation and eliminated unnecessary busy-loops in the scraper queue lower idle power consumption.
- **Pagination improvements**: Source switching and search result display are more reliable, avoiding duplicate network requests and showing items faster.
- All improvements from version 0.0.47 remain active, including Android Auto experience enhancements, playback reliability fixes, customizable car controls, unified audiobook timeline, refined artwork consistency, safer shutdown, improved connection resilience, cleaner error handling for protected links, and better download recognition.

### Behavior changes

- Sleep timer volume fade uses linear curve instead of cosine — fade behavior may sound slightly different at the end of the fade-out.

### BREAKING CHANGES

None

### Risks / What to test

- Sleep timer fade behavior (linear vs cosine curve) sounds acceptable during end-of-timer fade-out
- Library scroll positions restore correctly after app restart
- App returns from background with library still populated (no empty screen)
- Pagination loads correctly when switching between sources and search results

## Русский

- **Восстановление позиций прокрутки библиотеки**: Позиции прокрутки сетки теперь корректно сохраняются при перезапуске приложения, и вы возвращаетесь туда, где остановились.
- **Больше нет пустого экрана после фона**: Обработка давления памяти больше не очищает загруженные элементы библиотеки, поэтому приложение сразу показывает ваши книги при возвращении.
- **Улучшено поведение таймера сна**: Затухание звука при таймере сна теперь использует линейную кривую громкости для более равномерного снижения слышимой громкости.
- **Обновлены тактильные сигналы**: Вибрация при нажатии кнопок использует новый паттерн для более четкого тактильного отклика.
- **Снижено потребление CPU**: Более медленная анимация индикатора прогресса и устранение ненужных циклов ожидания в очереди скрейпера снижают потребление энергии в режиме ожидания.
- **Улучшения пагинации**: Переключение между источниками и отображение результатов поиска стали надежнее, исключаются дублирующие сетевые запросы, а элементы отображаются быстрее.
- Все улучшения версии 0.0.47 остаются активными, включая улучшения опыта Android Auto, исправления надежности воспроизведения, настраиваемые элементы управления автомобилем, унифицированную временную шкалу аудиокниг, уточненную согласованность обложек, более безопасное завершение работы, улучшенную устойчивость подключений, более чистую обработку ошибок для защищенных ссылок и лучшее распознавание загрузок.

### Изменения поведения

- Затухание громкости таймера сна использует линейную кривую вместо косинусной — поведение затухания может звучать немного иначе в конце затухания.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ

Нет

### Риски / Что проверить

- Поведение затухания таймера сна (линейное vs косинусное) звучит приемлемо во время затухания в конце таймера
- Позиции прокрутки библиотеки корректно восстанавливаются после перезапуска приложения
- Приложение возвращается из фона с заполненной библиотекой (без пустого экрана)
- Пагинация корректно загружается при переключении между источниками и результатами поиска
