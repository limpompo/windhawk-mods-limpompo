# Explorer: open new windows as tabs

**English** | [Русский](README.ru.md)

When a new File Explorer window is opened (Win+E, "Open in new window", "Show in folder" from another program, a folder from the desktop, a shortcut, etc.) and another visible Explorer window already exists, this [Windhawk](https://windhawk.net) mod hides the new window and:

- if the folder is already open in some tab - makes that tab active;
- otherwise - adds a new tab to the topmost Explorer window and opens the folder there.

## Features

- Selected files ("Show in folder") are selected in the tab as well.
- Fixes "Show in folder" for an already open folder: Explorer selects the file but neither switches to the tab nor always picks the right one. The mod switches to the correct tab.
- New tabs are opened with the "Open in new tab" command, like the context menu does.
- Not merged: a window created while the left mouse button is held (a tab dragged out into its own window) and windows on another virtual desktop.
- If anything goes wrong, the new window is shown as usual.

## Settings

| Setting | Default | What it does |
|---|---|---|
| Do not open a folder twice | on | Switch to the tab if the folder is already open |
| Switch to the tab where the program selected a file | on | Fixes "Show in folder" tab switching |
| Bring the tabbed window to the foreground | on | Activate (and restore) the Explorer window |
| Leave windows created with a mouse button held | on | Protects dragged-out tabs |

## Requirements

- Windows 11 22H2 or newer (File Explorer with tabs).
- [Windhawk](https://windhawk.net).

## Known limitations

The "new tab" window command (`WM_COMMAND 0xA21B`) and part of the logic rely on undocumented Explorer behavior, so a future Windows build may break the mod.

## Installation

1. Install [Windhawk](https://windhawk.net).
2. In Windhawk click **Create a new mod**, replace the generated code with the contents of [`explorer-windows-to-tabs.wh.cpp`](explorer-windows-to-tabs.wh.cpp), then click **Compile Mod** and **Enable**.

The mod is being submitted to the official Windhawk catalog. Once it is accepted it can be installed directly: **Explore** -> search for **Explorer: open new windows as tabs** -> **Install**.

## License

[MIT](../../LICENSE)
