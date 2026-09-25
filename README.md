# DataWedgeSample

DataWedgeSample is a single HTML page for checking how a Zebra DataWedge barcode scanner delivers data to a web page. DataWedge can be configured to send scanned barcodes as keystrokes, and a web app that relies on this needs to know exactly which key events arrive and how the end of a scan is signalled. This page listens for `keypress` events on the document, appends each received character to an on-screen output area and starts a new line when it receives Enter (key code 13), which the code treats as the Enter sent by DataWedge at the end of a scan. It also logs the key codes of every `keydown`, `keypress` and `keyup` event to the browser console. It is meant for developers who are integrating Zebra handheld scanners with a browser-based app and want a quick way to verify their DataWedge profile on the device. It is written in plain HTML and inline JavaScript with no dependencies or build step, and is a small, finished demo from March 2024.

**Live demo:** https://www.rach.im/DataWedgeSample/

## Features

- Listens for `keypress` and appends each character (`event.key`) to the output area; Enter (key code 13) adds a line break
- Checkbox to add or remove the `keypress` listener at runtime
- Logs `keydown`, `keypress` and `keyup` key codes to the browser console
- Viewport meta tag set up for handheld screens, with wrapped output text
- No dependencies and no build step

## Tech stack

HTML · vanilla JavaScript · CSS · GitHub Pages

## Usage

1. On the Zebra device, set the DataWedge profile used by the browser to keystroke output (optionally with an Enter suffix).
2. Open the live demo, or `index.html`, in that browser.
3. Scan a barcode. Each scanned value appears under **Output**, one line per Enter key.
4. Untick **Listen for KeyPress?** to stop capturing, and reload the page to clear the output.

To run it locally, open `index.html` directly in a browser or serve the folder with any static file server.

## Project structure

```text
index.html        The demo page
docs/index.html   Identical copy served by GitHub Pages (master branch, /docs)
```

When you change the page, update both files.
