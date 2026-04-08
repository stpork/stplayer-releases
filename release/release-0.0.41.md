# Release notes — 0.0.41

Release date: 27-Mar-2026 

## English
- Reduced the app's tracking-related footprint by removing advertising ID access that could be added by bundled libraries.
- Removed unused ad attribution and install-referrer permissions, so the app asks for less advertising-related access.
- Removed unused ad-services components from the shipped package, keeping this release more privacy-focused.

### Behavior changes
- No workflow-visible changes. Playback, browsing, downloads, and history should behave the same as in 0.0.40.

### BREAKING CHANGES
- None

### Risks / What to test
- Install or update the app and confirm the permission/privacy listing no longer shows ad-related access.
- Smoke-test playback, browsing, downloads, and history to confirm no behavior changed.
- Verify the app still installs and opens normally after updating from 0.0.40.

## Русский
- Уменьшен связанный с отслеживанием след приложения: убран доступ к рекламному идентификатору, который могли добавлять встроенные библиотеки.
- Удалены ненужные разрешения для атрибуции рекламы и определения источника установки, поэтому приложению требуется меньше рекламно-ориентированного доступа.
- Из релизного пакета убраны неиспользуемые ad-services компоненты, что делает этот выпуск более приватным.

### Изменения в поведении
- Видимых изменений в сценариях работы нет. Воспроизведение, просмотр каталога, загрузки и история должны работать так же, как в 0.0.40.

### Ломающие изменения
- Нет

### Риски / Что проверить
- Установить или обновить приложение и проверить, что в списке разрешений/данных больше не показывается доступ, связанный с рекламой.
- Кратко проверить воспроизведение, просмотр каталога, загрузки и историю, чтобы убедиться, что поведение не изменилось.
- Убедиться, что приложение по-прежнему нормально устанавливается и запускается после обновления с 0.0.40.