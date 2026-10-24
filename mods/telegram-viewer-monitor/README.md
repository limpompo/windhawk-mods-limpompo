# Telegram: media viewer on the chat monitor

**English** | [Русский](README.ru.md)

Telegram Desktop remembers which monitor the media viewer was opened on and opens it there again, even if the main window has moved to another monitor. This [Windhawk](https://windhawk.net) mod opens Telegram's secondary windows (photo/video viewer, etc.) on the monitor where the main window is.

## Features

- Moves a secondary Telegram window to the main window's monitor before it is shown, so it doesn't flash on the old monitor.
- The window keeps its relative position (a window in a corner stays in the same corner of the other monitor); a window larger than the target monitor is shrunk to fit.
- A fullscreen window stays fullscreen; a maximized window stays maximized and, when restored, stays on the new monitor.
- Monitors with different scaling (for example 100% and 150%) are taken into account.
- Telegram data and system files are not modified.

## Settings

| Setting | Default | What it does |
|---|---|---|
| Keep window position | on | On: the window keeps its place (a corner stays a corner). Off: the window is centered on the main window's monitor |
| Account for monitor scaling | on | Places the window so it fits after Telegram resizes it for a different scale (100% / 150%). Turn off if windows are placed wrongly on such a setup |
| Window title filter | empty | Move only windows whose title contains this text; empty - all secondary windows |

## Which windows are moved

By default **all** secondary Telegram windows, not only the media viewer: also picture-in-picture video, call windows and chats opened in a separate window. If you keep some of them on another monitor on purpose, use the **Window title filter** setting to move only windows whose title contains the given text. Window titles follow Telegram's interface language, so the filter works only for that language.

## Requirements

- Telegram Desktop (`Telegram.exe`) on Windows.
- [Windhawk](https://windhawk.net).

## Installation

1. Install [Windhawk](https://windhawk.net).
2. In Windhawk click **Create a new mod**, replace the generated code with the contents of [`telegram-viewer-monitor.wh.cpp`](telegram-viewer-monitor.wh.cpp), then click **Compile Mod** and **Enable**.

The mod is being submitted to the official Windhawk catalog. Once it is accepted it can be installed directly: **Explore** -> search for **Telegram: media viewer on the chat monitor** -> **Install**.

## License

[MIT](../../LICENSE)
