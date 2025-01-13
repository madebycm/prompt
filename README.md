# Prompt File Processor

A command-line utility that combines multiple text files into a single prompt file, making it easier to work with large codebases in AI interactions.

## Description

This bash script helps you prepare text files for AI interactions by:
- Combining multiple files into a single `prompt.txt` file
- Adding file headers and separators for clarity
- Automatically filtering out binary files and large files (>1MB)
- Supporting various filtering and selection options

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/prompt.git
cd prompt

# Make the script executable
chmod +x prompt
```

## Usage

The script can be used in several ways:

```bash
prompt                     # Process all text files in current directory
prompt --ignore main.dart  # Process everything except main.dart
prompt home.dart          # Find and process a single file
prompt lib/              # Process all files in lib/ directory
prompt "*.dart"          # Process all dart files recursively
prompt home.dart,settings.dart  # Process specific files
```

### Features

- Recursive file searching in current directory
- Automatic skipping of binary files and files >1MB
- File headers in output for better organization
- Support for file patterns and directory processing
- Ignore specific files with --ignore flag
- Outputs to `prompt.txt` in the current directory

### Notes

- The script automatically ignores itself and the output file (`prompt.txt`)
- Binary files and files larger than 1MB are skipped
- File paths are cleaned (double slashes removed)
- Each file in the output is preceded by a header with its path

## License

This project is licensed under the MIT License - see the LICENSE file for details.