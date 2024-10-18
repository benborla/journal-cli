# Daily Journal Bash Script

A simple, customizable bash script for managing daily journal entries from the command line.

## Features

- Create and edit daily journal entries
- Customizable journal location
- Configurable text editor
- List all existing journal entries
- Support for creating entries for specific dates
- Direct editing of configuration file

## System Requirements

- macOS or Unix-like operating systems (Linux, BSD, etc.)
- Bash shell

## Installation

1. Clone this repository or download the `journal` script.
2. Make the script executable:

   ```
   chmod +x journal
   ```

3. Move the script to a directory in your PATH for easy access:

   ```
   mv journal /usr/local/bin/journal
   ```

## Configuration

The script uses a configuration file located at `~/.journal_config`. You can set the following options:

- `JOURNAL_DIR`: Directory where journal entries are stored (default: `~/journal`)
- `DATE_FORMAT`: Format for date in filenames (default: `%m-%d-%Y`)
- `EDITOR`: Preferred text editor (default: `nvim`)

You can change these settings using the script's command-line options or by directly editing the configuration file.

## Usage

### Basic Usage

Create or edit today's journal entry:

```
journal
```

### Options

- `journal [DATE]`: Open journal for a specific date (format: MM-DD-YYYY)
- `journal yesterday`: Open yesterday's journal
- `journal --list`: List all journal entries
- `journal --set-journal-dir [DIR]`: Set custom journal directory
- `journal --set-editor [EDITOR]`: Set preferred text editor
- `journal --edit-config`: Edit the configuration file directly
- `journal --help`: Display help message
- `journal --version`: Display version information

### Examples

1. Create/edit today's entry:

   ```
   journal
   ```

2. Open entry for a specific date:

   ```
   journal 10-18-2024
   ```

3. List all entries:

   ```
   journal --list
   ```

4. Set custom journal directory:

   ```
   journal --set-journal-dir ~/Documents/MyJournal
   ```

5. Change default editor to vim:

   ```
   journal --set-editor vim
   ```

6. Edit configuration file:

   ```
   journal --edit-config
   ```

## Default Editor

The default editor is set to `nvim` (Neovim). You can change this by using the `--set-editor` option or by editing the configuration file with the `--edit-config` option.

## Compatibility

This script is designed to work on macOS and other Unix-like operating systems. It has been tested on macOS and common Linux distributions. Windows users might be able to use it through WSL (Windows Subsystem for Linux), but this is not officially supported.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

Ben Borla

## Acknowledgments

- Inspired by the daily journaling practice
- Thanks to the Bash scripting community for inspiration and resources
