# repo2txt

## Overview
`repo2txt` is a Python script I developed to help me facilitate an easy method of supplying training data to GPT-style Large Language Models (LLMs) that I was working with. The script automates the combining of assets in project or a project repository, generating one comprehensive text file and/or Word document that can be fed beck to the ingestor in one shot. The created file includes both a hierarchical tree of the directory structure and the contents of each file. My goal in creating repo2txt was to simplify the process of supplying codebases for AI training or anlalitic purposes, and I hope this tool will be helpful to you.

## Features
- **Directory/File Tree**: Generates a high-level overview of the repository's directory and file structure.
- **Detailed Contents**: Provides the full content of each file, offering insights into the code or text within the repository.
- **Output Formats**: Supports creating documentation in both `.txt` and `.docx` formats.
- **Customizable Ignoring Mechanism**: Allows specification of file types, individual files, and directories to ignore (e.g., binary files, temporary files, specific directories like `node_modules`).
- **Command-Line Flexibility**: Offers various command-line arguments to tailor the script's functionality.


## Suggested Installation
For ease of use install with pip

pip install repo2txt

But if you wish you can just copy the repo2txt.py file and run it that way. If you using this method please remember to install python-docx.

## Usage

Run the script from the command line, specifying the path to the repository and the desired output file name. For example:

```bash
python repo2txt.py [path_to_repo] [output_file_name]
```

Replace `[path_to_repo]` with the path to your cloned repository and `[output_file_name]` with your desired output file name (with `.txt` or `.docx` extension).

By default if you do not specify any path it will run inside the directory it is in and will drill down. 

By default if you do not specify the name of the output file it will be output.txt.


### Optional Command-Line Arguments:

- `--ignore-files`: List of file names to ignore (e.g., `--ignore-files file1.txt file2.txt`).
- `--ignore-types`: List of file extensions to ignore (e.g., `--ignore-types .log .tmp`).
- `--exclude-dir`: List of directory names to exclude (e.g., `--exclude-dir dir1 dir2`).
- `--ignore-settings`: Flag to ignore common settings files.
- `--include-dir`: Include only a specific directory and its contents (e.g., `--include-dir src`).

### Examples

1. **Documenting a Repository to a Text File**:
   ```bash
   python repo2txt.py /path/to/repository output.txt
   ```

2. **Documenting with Exclusions**:
   ```bash
   python repo2txt.py /path/to/repository output.docx --ignore-types .log .tmp --exclude-dir tests
   ```

## Contributing
Contributions to enhance `repo2txt` are welcome. Feel free to fork the repo, make your changes, and submit a pull request.

---
