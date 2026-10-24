# Changelog / Список изменений

## 1.1

- EN: The window is moved before it is shown (fixes the `SetWindowPos` path: the window was activated first and then not moved, or visibly jumped).
- EN: Keeps the window's relative position instead of centering it; accounts for monitors with different DPI scaling.
- EN: Maximized windows stay maximized on the new monitor and restore there; they are no longer treated as fullscreen.
- EN: Title filter setting without the 127-character limit and without a race on settings change; type-safe hooks (`WindhawkUtils::SetFunctionHook`).
- EN: README describes which windows are moved; the filter description notes that titles depend on Telegram's language.
- EN: New on/off settings: keep window position, account for monitor scaling, keep maximized windows maximized (all on by default).
- RU: Окно переносится до показа (исправлен путь через `SetWindowPos`: окно сначала активировалось и не переносилось или заметно прыгало).
- RU: Окно сохраняет своё положение вместо центрирования; учитываются мониторы с разным масштабом.
- RU: Развёрнутые окна остаются развёрнутыми на новом мониторе и восстанавливаются там же; больше не считаются полноэкранными.
- RU: Фильтр по заголовку без ограничения в 127 символов и без гонки при смене настроек; типобезопасные хуки.
- RU: В README описано, какие окна переносятся; в описании фильтра — что заголовки зависят от языка Telegram.
- RU: Новые переключатели: сохранять положение окна, учитывать масштаб мониторов, развёрнутые окна — развёрнутыми (все включены по умолчанию).

## 1.0

- EN: Current public version. Source comments and metadata in English, Russian name and description via `@name:ru-RU` / `@description:ru-RU`.
- RU: Текущая публичная версия. Комментарии в коде и метаданные на английском, русские название и описание через `@name:ru-RU` / `@description:ru-RU`.
