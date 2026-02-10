# Folder Scanner

A command-line tool that scans a folder and generates a summary report with file statistics.

## Features

- Total file count and disk usage
- Largest file identification
- Breakdown of files by extension (count and size)
- Optional filtering by file extension
- Report saved to a text file

## Usage

```bash
python folder_scanner.py <folder> [-o OUTPUT] [-e EXTENSION]
```

### Arguments

| Argument | Description |
|---|---|
| `folder` | Path to the folder to scan (required) |
| `-o`, `--output` | Output report file path (default: `folder_report.txt`) |
| `-e`, `--extension` | Filter by file extension (e.g. `.js`, `.txt`) |

### Examples

Scan a folder:

```bash
python folder_scanner.py /path/to/folder
```

Scan and save the report to a custom file:

```bash
python folder_scanner.py /path/to/folder -o my_report.txt
```

Scan only `.txt` files:

```bash
python folder_scanner.py /path/to/folder -e .txt
```

The extension filter also works without the leading dot:

```bash
python folder_scanner.py /path/to/folder -e txt
```

## Sample Output

```
============================================================
           FOLDER SCAN REPORT
============================================================
Folder:       /Users/example/Downloads
Filter:       *.txt files only
Scanned at:   2026-02-10 10:00:00
------------------------------------------------------------
Total files:  3
Total size:   12.50 KB
Largest file: notes.txt (8.00 KB)
------------------------------------------------------------
FILE TYPES BREAKDOWN
  Extension             Count           Size
  -------------------- ------   ------------
  .txt                      3       12.50 KB
============================================================
```
