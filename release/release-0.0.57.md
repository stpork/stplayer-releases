# Release notes — 0.0.57

Release date: 23-Apr-2026

## English
- Production builds no longer write diagnostic log files to device storage, improving privacy and reducing unnecessary storage use.

### Behavior changes
- No log files are created on your device in the public release build. Diagnostic logging remains available only in development and testing builds.

### BREAKING CHANGES
- None

### Risks / What to test
- Verify the app does not create any log files on device storage after install and normal use.
- Verify playback, library, history, favorites, and settings continue to work as expected.

## Русский

# Примечания к выпуску — 0.0.57

Дата выпуска: 23-Apr-2026

## Русский
- В публичных сборках приложение больше не создаёт диагностические файлы журналов на устройстве — это улучшает приватность и уменьшает ненужное использование памяти.

### Изменения в поведении
- В публичной сборке файлы журналов не создаются в памяти устройства. Диагностическое логирование сохраняется только в сборках для разработки и тестирования.

### КРИТИЧЕСКИЕ ИЗМЕНЕНИЯ
- Отсутствуют

### Риски / Что проверить
- Убедиться, что после установки и обычного использования приложение не создаёт файлов журналов в памяти устройства.
- Проверить, что воспроизведение, библиотека, история, избранное и настройки работают как прежде.
