# Telegram: media viewer on the chat monitor

**English** | [Русский](README.ru.md)

Telegram Desktop remembers which monitor the media viewer was opened on and opens it there again, even if the main window has moved to another monitor. This [Windhawk](https://windhawk.net) mod opens Telegram's secondary windows (photo/video viewer, etc.) on the monitor where the main window is.

## Features

- Intercepts the showing of secondary Telegram windows and moves a window to the main window's monitor if it appeared on another one.
- A fullscreen window stays fullscreen on the target monitor.
- Optional filter by window title (setting **Window title filter**).
- Telegram data and system files are not modified.

## Requirements

- Telegram Desktop (`Telegram.exe`) on Windows.
- [Windhawk](https://windhawk.net).
## Installation

1. Install [Windhawk](https://windhawk.net).
2. Open Windhawk, go to **Explore** and search for **Telegram: media viewer on the chat monitor** (once the mod is published in the Windhawk catalog).
3. Click **Install**.

Manual installation (before the mod appears in the catalog): in Windhawk click **Create a new mod**, replace the generated code with the contents of [`telegram-viewer-monitor.wh.cpp`](telegram-viewer-monitor.wh.cpp), then **Compile Mod** and **Enable**.

## License

[MIT](../../LICENSE)
