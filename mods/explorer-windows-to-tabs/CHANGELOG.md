# Changelog / Список изменений

## 1.7

- EN: A tab closed in another Explorer window while a new window is being merged is no longer taken for a dragged-out tab: the tab that left must have the same title as the new window's tab.
- EN: "Show in folder": tabs showing the contents of an archive (.zip, .cab) are no longer probed.
- EN: The redirect state of "Show in folder" is per window thread (`thread_local`).
- EN: Setting descriptions say that the tab switch and window activation also happen when other programs (scripts, sync tools) select files in an Explorer window.
- RU: Вкладка, закрытая в другом окне Проводника во время слияния нового окна, больше не принимается за вытащенную: ушедшая вкладка должна называться так же, как вкладка нового окна.
- RU: «Показать в папке»: вкладки с содержимым архива (.zip, .cab) больше не проверяются.
- RU: Состояние перенаправления «Показать в папке» — своё у каждого потока окна (`thread_local`).
- RU: В описаниях настроек сказано, что переключение вкладки и вывод окна вперёд срабатывают и тогда, когда файлы в окне Проводника выделяют другие программы (скрипты, синхронизация).

## 1.6

- EN: Safe unloading: one long-lived worker thread does all merges and tab switches; `Wh_ModUninit` stops it and waits without a timeout; waits end at once on unload; tab hooks and UI Automation are released on the worker before it exits.
- EN: New windows are caught with a `CreateWindowExW` hook instead of WinEvent hooks (no hook thread, no callbacks after unload).
- EN: Only windows of this `explorer.exe` process are used as targets; tab hooks are installed without a module handle (can't load the DLL into other processes); no named event - commands are passed as a pointer in a registered message.
- EN: `@architecture x86-64`; the mod doesn't load on builds without Explorer tabs (before 22621).
- EN: "Show in folder": probing other tabs no longer clears their selection or moves focus, an item found in several tabs isn't redirected, and only file system tabs are probed (other folder types never receive a foreign item ID).
- EN: "Show in folder" into an already active tab now brings the Explorer window to the front (it used to stay behind the program, so nothing seemed to happen).
- EN: No duplicate tab when "Open in new tab" finishes late; a failed tab switch restores the tab that was active before it.
- EN: A tab dragged out into its own window is recognized by the tab leaving its old window (Explorer creates the window after the button is released and then destroys the old tab), so it is never merged back (closing a whole window at the same moment doesn't count); swapped mouse buttons are respected; a double-click is still merged.
- EN: When the last-resort tab switch fails, the previously active tab is restored.
- EN: New setting: hold Shift while opening a folder to get a separate window (on by default).
- EN: Control Panel is never merged and never used as the window to add a tab to.
- EN: Code: SDK GUIDs, `ComPtr`, `WindhawkUtils::SetFunctionHook`, test code removed. README compares the mod with Explorer Single Window Tabs.
- RU: Безопасная выгрузка: один постоянный рабочий поток выполняет все слияния и переключения; `Wh_ModUninit` останавливает его и ждёт без таймаута; ожидания прерываются сразу; хуки вкладок и UI Automation освобождаются в рабочем потоке до его выхода.
- RU: Новые окна ловятся хуком `CreateWindowExW` вместо WinEvent (нет потока хуков, нет обратных вызовов после выгрузки).
- RU: Цели — только окна этого процесса `explorer.exe`; хуки вкладок ставятся без модуля (DLL не затягивается в другие процессы); нет именованного события — команды передаются указателем в зарегистрированном сообщении.
- RU: `@architecture x86-64`; мод не загружается на сборках без вкладок Проводника (до 22621).
- RU: «Показать в папке»: проверка других вкладок больше не сбрасывает их выделение и не двигает фокус, элемент, найденный в нескольких вкладках, не перенаправляется, и проверяются только вкладки с папками файловой системы (другие папки не получают чужой идентификатор элемента).
- RU: «Показать в папке» в уже активную вкладку теперь выводит окно Проводника на передний план (раньше оно оставалось за программой, и казалось, что ничего не произошло).
- RU: Нет второй вкладки, если «Открыть в новой вкладке» отработало с задержкой; при неудачном переключении возвращается вкладка, активная до него.
- RU: Вытащенная вкладка распознаётся по тому, что она уходит из старого окна (Проводник создаёт окно после отпускания кнопки и затем уничтожает старую вкладку), поэтому она никогда не сливается обратно (закрытие целого окна в тот же момент не считается); переставленные кнопки мыши учитываются; двойной щелчок по-прежнему сливается.
- RU: Если последняя попытка переключения не удалась, возвращается вкладка, активная до неё.
- RU: Новая настройка: Shift при открытии папки — отдельное окно (включена по умолчанию).
- RU: Панель управления никогда не сливается и не выбирается окном, куда добавляется вкладка.
- RU: Код: GUID из SDK, `ComPtr`, `WindhawkUtils::SetFunctionHook`, тестовый код удалён. README сравнивает мод с Explorer Single Window Tabs.

## 1.5

- EN: Current public version. Source comments and metadata in English, Russian name and description via `@name:ru-RU` / `@description:ru-RU`.
- RU: Текущая публичная версия. Комментарии в коде и метаданные на английском, русские название и описание через `@name:ru-RU` / `@description:ru-RU`.
