# Changelog / Список изменений

## 2.1

- EN: Addressed the AI review: the mod unloads itself at once (`Wh_ModInit` returns `FALSE`) from processes that are not in the *Applications* list; the reload-on-change logic is reduced to unloading when an app is removed from the list. An app added to the list works after it is restarted.
- EN: The default application in the list is the placeholder `test.exe` instead of Telegram.exe.
- EN: Renamed "Child windows" to "Secondary windows" in the Russian name and texts.
- EN: README states that Telegram is the only tested app and that the window filter for non-Qt apps is a heuristic.
- RU: По замечаниям AI-ревью: мод сразу выгружается (`Wh_ModInit` возвращает `FALSE`) из процессов, которых нет в списке «Приложения»; логика перезагрузки сведена к выгрузке при удалении приложения из списка. Добавленное в список приложение работает после перезапуска.
- RU: Приложение в списке по умолчанию — заглушка `test.exe` вместо Telegram.exe.
- RU: В русском названии и текстах «Дочерние окна» заменено на «Второстепенные окна».
- RU: В README указано, что проверялся только Telegram, а фильтр окон для не-Qt приложений — эвристика.

## 2.1

- EN: Addressed the AI review: the mod now targets `Telegram.exe` (`@include telegram.exe`) and hooks unconditionally; other apps are added in the Advanced tab (*Custom process inclusion list*). The *Applications* setting, the process matching and the reload logic are removed.
- EN: The *Window title filter* is a single global setting again.
- EN: Renamed "Child windows" to "Secondary windows" in the Russian name and texts.
- EN: README states that Telegram is the only tested app and that the window filter for non-Qt apps is a heuristic.
- RU: По замечаниям AI-ревью: мод нацелен на `Telegram.exe` (`@include telegram.exe`) и ставит хуки безусловно; другие приложения добавляются на вкладке Advanced (*Custom process inclusion list*). Настройка «Приложения», сопоставление процессов и логика перезагрузки убраны.
- RU: «Фильтр по заголовку окна» снова одна общая настройка.
- RU: В русском названии и текстах «Дочерние окна» заменено на «Второстепенные окна».
- RU: В README указано, что проверялся только Telegram, а фильтр окон для не-Qt приложений — эвристика.

## 2.0

- EN: The mod works with any app, not only Telegram: the new *Applications* setting is a list of processes (Telegram.exe by default), each with its own window title filter. Renamed to "Secondary windows on the active monitor", new id `secondary-windows-on-active-monitor` (was `telegram-viewer-monitor`).
- EN: The mod is loaded into every process (`@include *`) but hooks only the processes from the list; changes to the list apply without restarting the apps.
- EN: Window filtering for non-Qt apps: menus, tooltips, drop-down lists, tool windows and non-activating windows are skipped.
- EN: The global *Window title filter* setting moved into each app entry.
- EN: README states that the mod is meant for multi-monitor setups and shows a demo.
- RU: Мод работает с любым приложением, а не только с Telegram: новая настройка «Приложения» — список процессов (по умолчанию Telegram.exe), у каждого свой фильтр по заголовку. Новое название — «Дочерние окна на активном мониторе», новый id `secondary-windows-on-active-monitor` (был `telegram-viewer-monitor`).
- RU: Мод загружается во все процессы (`@include *`), но ставит хуки только в процессах из списка; изменения списка применяются без перезапуска приложений.
- RU: Отбор окон для не-Qt приложений: меню, подсказки, выпадающие списки, панели инструментов и неактивируемые окна не переносятся.
- RU: Общая настройка «Фильтр по заголовку окна» перенесена в запись каждого приложения.
- RU: В README сказано, что мод нужен при нескольких мониторах, добавлена демонстрация.

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
