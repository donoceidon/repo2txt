# repo2txt

## Overview
`repo2txt` is a Python tool I assemble to help streamline the process of preparing training data for GPT-style Models (LLMs). It's especially helpful in passing a codebase to a GPT. This script automates the task of compiling assets from a project or repository into a single, comprehensive text file or Word document. The resulting file includes a hierarchical tree of the directory structure and the contents of each file.

## Features
- **Directory/File Tree**: Generates a detailed overview of the repository's directory and file structure.
- **File Contents**: Includes the content of each file, offering a comprehensive view into the code or text within the repository.
- **Output Formats**: Supports output in both `.txt` and `.docx` formats.
- **Customizable Ignoring Mechanism**: Provides options to ignore specific file types, individual files, and directories, allowing for a tailored documentation process.
- **Command-Line Flexibility**: Various command-line arguments are available to customize the script's output according to the user's needs.

## Suggested Installation
For ease of use, `repo2txt` can be installed via pip:

```bash
pip install repo2txt
```

Alternatively, you can directly run the `repo2txt.py` script. Ensure to install `python-docx` if using this method.

## Usage

Run the script from the command line by specifying the path to the repository and the desired output file name. For example:

```bash
python repo2txt.py -r [path_to_repo] -o [output_file_name]
```

Replace `[path_to_repo]` with the path to your repository and `[output_file_name]` with your desired output file name (including the `.txt` or `.docx` extension).

By default, if no path is specified, the script operates in the current directory. Similarly, if no output file name is provided, it defaults to `output.txt`.

### Optional Command-Line Arguments:

- `-r`, `--repo_path`: Specify the path to the repository. Defaults to the current directory if not specified.
- `-o`, `--output_file`: Name for the output file. Defaults to "output.txt".
- `--ignore-files`: List of file names to ignore (e.g., `--ignore-files file1.txt file2.txt`). Specify 'none' to ignore no files.
- `--ignore-types`: List of file extensions to ignore (e.g., `--ignore-types .log .tmp`). Defaults to a predefined list in `config.json`. Specify 'none' to ignore no types.
- `--exclude-dir`: List of directory names to exclude (e.g., `--exclude-dir dir1 dir2`). Specify 'none' to exclude no directories.
- `--ignore-settings`: Flag to ignore common settings files.
- `--include-dir`: Include only a specific directory and its contents (e.g., `--include-dir src`).

### Examples

1. **Documenting a Repository to a Text File**:
   ```bash
   python repo2txt.py -r /path/to/repository -o output.txt
   ```

2. **Documenting with Exclusions**:
   ```bash
   python repo2txt.py -r /path/to/repository -o output.docx --ignore-types .log .tmp --exclude-dir tests
   ```

## Contributing
Contributions to enhance `repo2txt` are always welcome. Feel free to fork the repository, make your improvements, and submit a pull request.
