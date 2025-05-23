### Overview

This Python program, `unifyTXT.py` is designed to organize CSV files from various subdirectories into a central directory structure based on specific categories, such as `backward`, `forward`, `landing`, `left`, `right`, and `takeoff`. The program processes directories containing BCI data, identifies files, moves them to appropriate folders, and deletes unnecessary `.csv` files.

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/J5JI_SrRVtA/0.jpg)](https://www.youtube.com/watch?v=J5JI_SrRVtA)

### Features

- Organizes TXT Files: Files are moved to corresponding directories like takeoff, backward, right, etc.
- Removes Duplicate Files: Duplicate `.txt` files are identified and deleted.
- Deletes CSV Files: All `.csv` files in the source directories are deleted.
- Cleans Up Empty Directories: Once the files are moved, empty subdirectories and group directories are removed.


### Usage

`unifyTXT.py` should be ran inside the same directory that the data directory is located. Line 81 of the program, `base_directory = "data"`, holds the name of the data folder. "data" can be changed depending on the name of the data folder.


### Example Directory Structure

```
data/
  group03/
    individual10/
      takeoff/
        BrainFlow-RAW_2025-02-28_11-59-05_5.txt
        OpenBCI-RAW-2025-03-12_14-46-24.csv
      backward/
        BrainFlow-RAW_backward_5_10.txt
  group04/
    Test 5/
      OpenBCISession_backward_5/
        BrainFlow-RAW_backward_5_10.txt
        OpenBCI-RAW-2025-03-12_14-46-24.csv
```

It is important to note that the "group" subdirectories are not name specific, meaning that they can have any given name. This also goes for the "individual" and "Test" subdirectories. The subdirectories located in "individual" and "Test" directories have various names, so the program must account for this. With the way that the program is currently written (3/21/2025), subdirectory names must follow this naming scheme:

- `backward` or `backwards`
- `forward`
- `landing`
- `left`
- `right`
- `takeoff` or `take_off`

This naming is not case sensitive (Ex. `TAKE_OFF` is allowed.), and the location of the word in the string does not matter (Ex. `OpenBCISession_takeoff_5/` is allowed.).

Note: updated according to the ticket: https://github.com/3C-SCSU/Avatar/issues/197
#### Author

Thomas Herold
