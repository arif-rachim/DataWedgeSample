# DataWedgeSample

A single HTML page for testing Zebra DataWedge keystroke output in a browser. When DataWedge sends scanned barcodes as key events, the page prints each character it receives and starts a new line on Enter.

**Live demo:** http://www.rach.im/DataWedgeSample/

## Features

- Listens for `keypress` and appends each character to an output area. Enter (key code 13) adds a line break
- Checkbox to turn the `keypress` listener on and off
- Logs `keydown` / `keyup` key codes to the browser console
- No dependencies and no build step

## Usage

Open the live demo, or `index.html`, in the browser on a Zebra device with DataWedge set to keystroke output, then scan a barcode. Reload the page to clear the output.

`docs/index.html` is an identical copy, served by GitHub Pages.
