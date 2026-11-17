# OSnagit

OSnagit is a Windows app for capturing your screen, marking up what you captured, and keeping everything in a searchable library. It is a screenshot and screen recording tool in the spirit of Snagit.

This repository holds the installers, checksums, and release notes. It does not contain source code.

## What it does

**Capture**
- Capture a region, a window, or a scrolling page, on any connected display, with global hotkeys.
- Record a screen region or a window to MP4, with optional microphone and system audio.
- Open existing PNG or JPG files with Open Image or by dragging them in from Explorer.

**Edit**
- Draw arrows, shapes, text, and numbered steps. Blur, pixelate, highlight, or spotlight parts of the image, and cover sensitive content with solid redactions.
- Crop, cut a strip out of the image, extend the canvas, and resize the output.
- Pick a quick style for each tool, work with layers, and sample colors from the image.
- Undo and redo every change. The original image is kept next to your edits.
- Save work as an editable `.osnag` project so you can reopen it later.

**Library**
- Every capture and recording is kept in a library you can filter by type, year, month, or tag, and sort by date, name, or size.
- Pin captures, tag them, and save filter presets.
- A Recent strip under the editor gives quick access to the latest captures.

**OCR**
- Text in captures is read with a bundled Tesseract engine, so you can search the library by what the images say. The index is built from the rendered image, so text you redacted can't be found through search.
- Copy text out of a capture, or scan QR codes and barcodes in it.

**Other**
- The interface is available in Thai and English, with dark and light themes.

## Install

1. Download `OSnagit-<version>-x64-setup.exe` from the [latest release](../../releases/latest).
2. Run the installer. It includes the .NET runtime and OCR data, so nothing else needs to be installed.

Requirements: Windows 10 version 19041 or later, x64.

## Updates

OSnagit checks this repository for a newer release when it starts, at most once every 24 hours. You can also check at any time from **Settings > General**. Nothing is downloaded until you choose to, and the installer is verified against its SHA-256 checksum before it runs.

## Verify a download

Each release includes `SHA256SUMS.txt`. In PowerShell:

```powershell
Get-FileHash .\OSnagit-<version>-x64-setup.exe -Algorithm SHA256
```

The hash should match the line in `SHA256SUMS.txt`. The installer is not code signed, so Windows SmartScreen may warn you the first time you run it.
