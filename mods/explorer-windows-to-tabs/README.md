# Explorer: open new windows as tabs

**English** | [Русский](README.ru.md)

When a new File Explorer window is opened (Win+E, "Open in new window", "Show in folder" from another program, a folder from the desktop, a shortcut, etc.) and another visible Explorer window already exists, this [Windhawk](https://windhawk.net) mod hides the new window and:

- if the folder is already open in some tab - makes that tab active;
- otherwise - adds a new tab to the topmost Explorer window and opens the folder there.

## Features

- Selected files ("Show in folder") are selected in the tab as well.
- Fixes "Show in folder" for an already open folder: Explorer selects the file but neither switches to the tab nor always picks the right one. The mod switches to the correct tab.
- New tabs are opened with the "Open in new tab" command, like the context menu does.
- Hold **Shift** while opening a folder to get a separate window.
- Control Panel is never merged and never gets other folders added as tabs.
- Not merged: a tab dragged out into its own window, however fast the drag is (a tab leaves another window at the moment the new window appears), and windows on another virtual desktop. A folder opened by double-click is merged.
- If anything goes wrong, the new window is shown as usual.
- Turning the mod off is safe: all its work happens on one thread that is stopped and waited for.

## Compared to Explorer Single Window Tabs

[Explorer Single Window Tabs](https://windhawk.net/mods/explorer-single-window-tabs) also opens new Explorer windows as tabs. This mod additionally switches to a tab that already shows the folder, carries the "Show in folder" selection over to the new tab, fixes "Show in folder" into an already open folder, opens tabs with the "Open in new tab" verb, protects dragged-out tabs by the held mouse button (besides the Shift bypass that both mods have), and restores the new window if the tab couldn't be opened.

**Don't enable both mods at the same time** - they would both handle every new window.

## Settings

| Setting | Default | What it does |
|---|---|---|
| Do not open a folder twice | on | Switch to the tab if the folder is already open |
| Switch to the tab where the program selected a file | on | Fixes "Show in folder" tab switching |
| Bring the tabbed window to the foreground | on | Activate (and restore) the Explorer window |
| Hold Shift to open a separate window | on | Shift held while opening a folder - the window stays separate |
| Leave tabs dragged out into their own window | on | Protects dragged-out tabs; a double-click is still merged |

## Requirements

- Windows 11 22H2 or newer (File Explorer with tabs); on older builds the mod doesn't load.
- [Windhawk](https://windhawk.net).

## Known limitations

The "new tab" window command (`WM_COMMAND 0xA21B`) and part of the logic rely on undocumented Explorer behavior, so a future Windows build may break the mod.

## Installation

1. Install [Windhawk](https://windhawk.net).
2. In Windhawk click **Create a new mod**, replace the generated code with the contents of [`explorer-windows-to-tabs.wh.cpp`](explorer-windows-to-tabs.wh.cpp), then click **Compile Mod** and **Enable**.

The mod is being submitted to the official Windhawk catalog. Once it is accepted it can be installed directly: **Explore** -> search for **Explorer: open new windows as tabs** -> **Install**.

## License

[MIT](../../LICENSE)
