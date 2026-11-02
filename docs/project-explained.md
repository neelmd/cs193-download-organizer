# How the script will work

The script will sort files by their extensions. A PDF will go to Documents, a JPG to Images, and a ZIP to Archives. Other files will go to Other. A preview will show the moves. The --apply option will move the files.

## Example

Suppose a folder contains notes.pdf, photo.JPG, project.zip, and shopping-list.

| File | Destination |
| --- | --- |
| notes.pdf | Documents/notes.pdf |
| photo.JPG | Images/photo.JPG |
| project.zip | Archives/project.zip |
| shopping-list | Other/shopping-list |

The code is not written yet. Here is how I plan to run it:

- `bash organize.sh /path/to/folder` will print the planned moves.
- `bash organize.sh --apply /path/to/folder` will move the files.

If Documents/notes.pdf already exists, the script will skip notes.pdf. Both files will keep their contents and names.

## Diagram

1. Read the folder path and options. Stop if the input is invalid.
2. Find the files directly inside the folder. Ignore hidden files, subfolders, and symbolic links.
3. Read each file extension and choose its category.
4. For a preview, print the move. For --apply, check the destination name, create the category folder, and try the move.
5. Repeat for the next file. Print the totals when there are no files left.

The script ignores subfolders, so a second run will leave the category folders alone.

## Matrix

- Do: features for the first version.
- Schedule: features to add later.
- Delegate: jobs that existing commands can do.
- Delete: features I will leave out.

## Terms

| Term | Meaning |
| --- | --- |
| Bash script | A text file of commands run in the terminal. |
| Terminal | The app where I type commands. |
| Extension | The part after the final dot, such as pdf or jpg. |
| --apply | The option that moves the files. |
| Preview | A list of the moves the script would make. |
| Symbolic link | A link to another file or folder. |
| mkdir -p | Creates a folder and any missing parent folders. |
| mv -n | Moves a file without replacing an existing file. |
| tr | Changes characters. I will use it to make extensions lowercase. |
| printf | Prints text in the terminal. |
| Git commit | A saved version of the project. |
| Minimum Viable Product (MVP) | The first useful version of the project. |

## Choices

Bash has commands for creating folders and moving files. I can use those commands in a script.

Preview mode lets me check the moves first. The destination-name check prevents a file from replacing an existing file.

The first version only sorts files directly inside one folder. Files inside subfolders stay where they are.

## Totals

- Planned: moves shown in preview.
- Moved: successful moves.
- Skipped: moves skipped because the destination name exists.
- Failed: operations that did not finish.

Hidden files, subfolders, and symbolic links are excluded before this loop.

## Final walkthrough

I need a working script and a 3-4 minute recording. I should be able to explain each command and show a preview, a file move, and a duplicate filename.
