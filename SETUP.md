# Filename Cleaner - Setup & Installation

## 1. Requirements

- Python 3.9 or newer recommended
- Unidecode Python package
- Windows, macOS, or Linux with Python installed

## 2. Install Dependencies

Open Command Prompt or a terminal and run:

```bash
python -m pip install unidecode
```

The script also checks whether Unidecode is installed when it starts. If it is missing, it displays the installation command and exits.

## 3. Project Files

Your project folder can be organized like this:

```text
Filename-Cleaner/
├── filename_cleaner.py
├── README.md
├── SETUP.md
└── LICENSE
```

## 4. Running the Program

Open Command Prompt in the project directory and run:

```bash
python filename_cleaner.py
```

The program will display a prompt asking for a folder path.

Example:

```text
=== Filename Cleaner ===
Enter the full folder path below (you can drag and drop the folder here):
Folder path:
```

Enter or drag and drop the folder you want to process.

## 5. What Gets Changed?

The program:
1. Scans the selected folder and its subfolders.
2. Converts non-English characters into English equivalents.
3. Removes punctuation and special characters.
4. Replaces repeated spaces with a single space.
5. Preserves the original file extension.
6. Renames files when necessary.

## 6. Duplicate Names

If a cleaned filename already exists, the program adds a numbered suffix.

For example:

```text
image.jpg
image (1).jpg
image (2).jpg
```

## 7. Error Folder

If a file cannot be renamed, the program attempts to move it into an `error` folder inside its original directory.

If moving the file also fails, the program prints an error message.

## 8. Important Safety Information

**This program changes filenames directly. It does not create backup copies.**

Before running it:
- Make a backup of important files.
- Test it on a small folder first.
- Check the results before processing large directories.
- Remember that other programs may rely on the original filenames.

There is currently no automatic undo feature.

## 9. Troubleshooting

### Unidecode Is Missing

Run:

```bash
python -m pip install --upgrade unidecode
```

### Invalid Folder Path

Make sure the folder exists and that the path is entered correctly.

### Permission Errors

Some files or folders may require additional permissions. Close applications using those files and check folder permissions.

### Files Could Not Be Renamed

The program attempts to move failed files into an `error` folder. If that also fails, the error is printed in the terminal.
