# Changelog / Список изменений

## 1.2

- EN: Removed the "Keep maximized windows maximized" setting: maximized windows are always moved as maximized (turning it off only brought back broken behavior).
- EN: Moving to a monitor with higher scaling no longer makes the window larger than the screen: the size is set so that it fits after Telegram rescales the window.
- EN: The restore rect of a maximized window gets the size for the new monitor's scaling, so the restored window keeps its visual size.
- RU: Убрана настройка «Развёрнутые окна — развёрнутыми»: развёрнутые окна всегда переносятся развёрнутыми (её выключение лишь возвращало ошибочное поведение).
- RU: При переносе на монитор с бо́льшим масштабом окно больше не выходит за экран: размер задаётся так, чтобы окно поместилось после того, как Telegram изменит его под новый масштаб.
- RU: Размер развёрнутого окна для восстановления пересчитывается под масштаб нового монитора, поэтому восстановленное окно не уменьшается.

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
