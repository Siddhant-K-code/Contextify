# Contextify

Contextify is a Python script designed to streamline the process of providing context to Large Language Models (LLMs) from your project files. It's particularly useful when working on coding tasks with LLMs, as it can automatically gather and format relevant code from your project.

## Features

- Selectively processes files in a directory, respecting `.gitignore` patterns
- Focuses on TypeScript files (`.ts` and `.tsx`)
- Ignores common directories and files that typically don't need to be included
- Outputs processed file contents in Markdown format
- Saves output to a Markdown file

## Requirements

- Python 3.x

## Usage

1. Place the `contextify.py` file in your project directory or set the `directory_path` variable in the script to point to your project directory.

2. Run the script:
   ```
   python contextify.py
   ```

3. The script will process the files and:
   - Print the output to the console
   - Save the output to `output.md` in the same directory

## Customization

You can customize the script by modifying the following variables:

- `directories_to_ignore`: List of directories to exclude from processing
- `files_to_ignore`: List of specific files to exclude from processing
- `extensions_to_include`: List of file extensions to include (currently set to `.ts` and `.tsx`)

## How It Works

1. The script walks through the specified directory and its subdirectories.
2. It filters files based on the ignore lists and included extensions.
3. For each included file, it reads the content and formats it in a Markdown code block.
4. The formatted content is collected in a single string.
5. The resulting string is printed, saved to a file.
