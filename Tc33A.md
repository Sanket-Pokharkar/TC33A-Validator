# TC33A Fixed-Width File Visualizer

## Overview

The TC33A Fixed-Width File Visualizer is a browser-based tool designed to simplify the analysis of TC33A files.

The tool transforms a fixed-width TC33A file into a color-coded view where each field is highlighted according to the applicable CP and TCR specification.

It helps QA engineers, developers, and business analysts identify field boundaries without manually counting character positions.

---

## Purpose

TC33A files use fixed-width records, where each physical line generally contains 168 characters.

Manually identifying field positions in these records can be difficult, especially when:

- The file contains multiple transactions.
- The file contains multiple CP and TCR records.
- Several fields contain only spaces.
- Field values must be verified using exact positions.
- Continuation TCR records do not repeat the CP application code.

The TC33A Visualizer makes these fields easier to identify by applying colors to every field and displaying relevant field details on hover.

---

## How It Works

1. Open the standalone HTML file in Microsoft Edge or Google Chrome.
2. Paste the complete TC33A file into the input text area.
3. Ensure that every physical TC33A record is on a separate line.
4. Click **Transform**.
5. The transformed file opens in a full-screen color-coded viewer.
6. Spaces in the original file are displayed as hyphens.
7. Hover over any colored field to view its field details.
8. Double-click a field to select only that field value.
9. Press `Ctrl+C` to copy the selected field.
10. Click **Exit Full Screen** or press `Esc` to return to the input screen.

---

## Main Features

- Supports complete TC33A files containing multiple transactions.
- Displays the transformed file in a full-screen viewer.
- Preserves the original file structure and line order.
- Displays all records in one continuous text-editor-style view.
- Uses a fixed-width font to preserve field alignment.
- Automatically replaces spaces with visible hyphens in the transformed view.
- Highlights every field using a light pastel background color.
- Ensures that adjacent fields use different colors.
- Automatically identifies CP and TCR record layouts.
- Shows field name, position, and length on hover.
- Allows field-only text selection using double-click.
- Supports copying the original file, transformed file, or selected field.
- Displays line numbers in a separate gutter.
- Identifies valid, invalid-length, and unknown-layout records.
- Fits all 168 characters within the available screen width.
- Processes all transaction data locally in the browser.
- Does not require a backend, database, installation, or internet connection.

---

## Input Requirements

The input must follow these rules:

- Paste the complete TC33A file into the input text area.
- Each TC33A physical record must be on a separate line.
- Each standard TC33A record should contain exactly 168 characters.
- The input file can contain actual spaces.
- Leading spaces, trailing spaces, and blank fixed-width fields must be preserved.
- Tabs should not be used because tab width can differ between editors.
- HTML tags or rich-text formatting should not be included in the TC33A data.

The tool does not modify the original input internally.

---

## Transform Behavior

After clicking **Transform**:

- The input area and other unnecessary page sections are hidden.
- The transformed file uses the complete available browser screen.
- All TC33A records remain in their original order.
- All fields are highlighted according to their applicable specification.
- Actual spaces are displayed as hyphens.
- The font size is automatically adjusted so that a standard 168-character record fits within the available screen width.
- Horizontal scrolling is minimized or removed for standard 168-character records.
- Vertical scrolling remains available for large files.

---

## Space Representation

Spaces are replaced with hyphens only in the transformed display.

### Original value