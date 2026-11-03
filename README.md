# Filename Cleaner

A lightweight Python utility that cleans filenames by converting non-English characters into English equivalents and removing unwanted symbols.

Filename Cleaner recursively scans a selected directory and renames files while preserving their extensions.

## Features

- **Transliteration:** Converts non-English characters into their closest English equivalents.
- **Character cleanup:** Removes punctuation and special characters.
- **Consistent naming:** Keeps only English letters, numbers, and spaces.
- **Extension preservation:** Keeps the original file extension.
- **Recursive scanning:** Processes files inside subfolders.
- **Duplicate handling:** Adds numbered suffixes when a filename already exists.
- **Error handling:** Attempts to move files that fail to rename into an `error` folder.
- **Simple operation:** Enter a folder path directly into Command Prompt.

## Example

| Original Filename | Cleaned Filename |
|---|---|
| `café photo.jpg` | `cafe photo.jpg` |
| `my_image!2026.png` | `my image 2026.png` |
| `東京旅行.jpg` | `Dong Jing Lu Xing.jpg` |
| `hello---world!!.txt` | `hello world.txt` |

Transliteration results depend on the characters and the Unidecode library.

## Requirements

- Python 3
- Unidecode

## Installation

Install the required dependency:

```bash
python -m pip install unidecode
```

See [SETUP.md](SETUP.md) for detailed instructions.

## Usage

Run the script:

```bash
python filename_cleaner.py
```

Enter the full path to the folder you want to process when prompted.

You can also drag and drop a folder into the Command Prompt window.

The program will scan the selected folder and its subfolders, renaming files as needed.

## Duplicate Filename Handling

If a cleaned filename already exists, the program automatically adds a number to make it unique.

For example:

```text
photo.jpg
photo (1).jpg
photo (2).jpg
```

## Error Handling

If a rename operation fails, the program attempts to move the affected file into an `error` folder within its original directory.

If that move also fails, an error message is printed.

## Important Notes

- Files are renamed directly, not copied.
- Original filenames are not automatically saved in a backup or undo log.
- Renaming may affect applications or shortcuts that depend on the original filenames.
- The `error` folder may be created inside scanned directories.
- Always test with a backup before processing important files.

## License

This project is licensed under the MIT License.
