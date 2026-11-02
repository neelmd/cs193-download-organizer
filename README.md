# Download Organizer

Downloads can pile up in one folder. This Bash script will sort them by file type and preview the moves.

## MVP

- Sort files into Documents, Images, Archives, and Other.
- Preview moves. Use --apply to move files.
- Skip existing destination names.
- Leave hidden files, subfolders, and symbolic links alone.

## Tech stack

Bash on macOS: `mkdir -p`, `mv -n`, `tr`, and `printf`. Files stay in local folders.

## Future plans

Custom categories, a move log, and an undo command.

## Documents

[Design PDF](docs/design.pdf) | [Matrix](docs/eisenhower-matrix.md) | [Build plan](docs/build-plan.md) | [Diagram](docs/system-diagram.png) | [Excalidraw file](docs/system-diagram.excalidraw)
