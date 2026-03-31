# SK Batch File Mover

A Windows desktop app for batch-organizing assets by naming convention.

## Features

- **Batch file moving** - Move files from a source directory to structured destination folders based on configurable naming rules
- **Preview before moving** - See exactly where files will go before committing
- **Configurable naming convention** - Define filename templates with placeholders (e.g. `{type}_{category}_{action}_{desc}_{variation}`) and destination folder structure (e.g. `{type}/{category}`)
- **Pre-move and post-move scripts** - Run custom scripts before and after file operations (e.g. validation, Wwise import)
- **Manifest output** - Generates a JSON manifest of moved files for script integration
- **Persistent settings** - Configuration saved to `file_mover_config.json` next to the executable

## Download

Get the latest release from the [Releases](https://github.com/silver-rain-dev/sk-batch-file-mover/releases) page.

## Getting Started

1. Download and extract `sk-batch-file-mover.zip` from the latest release
2. Run `file_mover_app.exe`
3. Set your source and destination directories
4. Configure your naming convention in Settings
5. Preview and move files

## Configuration

Settings are stored in `file_mover_config.json` in the same directory as the executable.

### Naming Convention

| Setting | Description | Example |
|---------|-------------|---------|
| Delimiter | Character separating filename parts | `_` |
| Filename template | Placeholders for filename parts | `{type}_{category}_{action}_{desc}_{variation}` |
| Destination template | Folder structure from filename parts | `{type}/{category}` |
| File extension | File type to process | `.wav` |

### Scripts

| Setting | Description |
|---------|-------------|
| Pre-move script | Runs before files are moved. If it fails, the move is aborted. |
| Post-move script | Runs after files are moved. |

Both scripts receive a JSON manifest (`skdam_move_manifest.json`) with the list of files and their parsed name parts.

## License

MIT
