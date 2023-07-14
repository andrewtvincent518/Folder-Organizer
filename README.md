# Folder Organizer

This repository contains a Python script that organizes files in a specified folder by moving them to corresponding subdirectories based on their file extensions.

## Prerequisites

Make sure you have the following installed before running the script:
- Python 3.x
- `json` module (usually included in the Python standard library)

## Usage

Follow the steps below to use the script:

1. Clone the repository to your local machine.
2. Navigate to the repository directory.

```bash
$ cd Folder-Organizer
```

3. Make sure you have a `file_formats.json` file in the same directory as the script. This file should contain a mapping of file extensions to target directories. For example:

```json
{
  ".txt": "text_files",
  ".jpg": "image_files",
  ".py": "python_files"
}
```

4. Open a terminal or command prompt and run the script by specifying the target folder as an argument.

```bash
$ python clean_folder.py /path/to/target_directory
```

Make sure to replace `/path/to/target_directory` with the actual path of the folder you want to clean.

## How it Works

The script performs the following steps:

1. Reads the `file_formats.json` file to obtain the file extension to target directory mapping.
2. Lists the contents of the target directory.
3. Iterates over each file in the target directory.
4. Skips any subdirectories encountered.
5. Checks the file extension of each file and verifies if it matches any of the file formats specified in `file_formats.json`.
6. If a match is found, creates the target directory (if it doesn't exist already).
7. Copies the file to the corresponding target directory.
8. Removes the original file from the target directory.
9. Prints an error message if any exception occurs during the process.
10. Prints a completion message after the cleaning process finishes.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use and modify the code according to your needs.

## File Formats

The `file_formats.json` file in this repository contains the mapping of file extensions to target directories. You can modify this file to customize the organization of your files.
