# Download Organizer

## Goal

Organize downloads so files are easier to find.

## MVP

- Sort files into Documents, Images, Archives, and Other.
- Preview moves. Move files only with --apply.
- Skip existing destination names.
- Ignore hidden files, subfolders, and symbolic links.
- Print a summary after each run.

## Tech stack

Bash on macOS. Commands: `mkdir -p`, `mv -n`, `tr`, and `printf`. Files stay in local folders.

## Future plans

- Custom categories and file types.
- A text log of file moves.
- An undo command.

## Documents

- [Design PDF](docs/design.pdf)
- [Eisenhower matrix](docs/eisenhower-matrix.md)
- [Build plan](docs/build-plan.md)
- [Diagram](docs/system-diagram.png) and [Excalidraw file](docs/system-diagram.excalidraw)
