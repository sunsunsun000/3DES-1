# 3DES
A (simple) homebrew 3ds File Browser written in C

 - Top screen - main file Browser
 - Upper area of bottom screen - instructions
 - Lower area of bottom screen - debug output (look here if, for example, you try
to create a directory and nothing happens)

# Notes
- Deleting directories uses a recursive function, so if you have a large (very large)
amount of directories/files inside the directory you want to delete, it may end up
breaking

# Buttons
Things in the buttons list below that are labelled as `not supported` have the
possibility of being added at a future date but are not definitely going to be implemented.

- A - Change to selected directory (opening files not supported)
- B - go "up" a directory
- X - CD to `/` and reallocate memory
- L - Create a new directory (brings a keyboard up to type the name)
- R - Delete file/directory
- DPAD/Circle pad up and down control the selection of files/directories
- DPAD/Circle pad left and right go to the top/bottom of the file/directory list
- START to close app and go back to HB menu

# TODO
- Check if memory has been allocated correctly after `malloc` & `realloc`
- Use [`strncpy()`](https://www.tutorialspoint.com/c_standard_library/c_function_strncpy.htm) instead of `strcpy()` to prevent overflow
- Fast scroll if you hold up/down
- Be able to select a file with Y then copy/paste to another path
- Put directories at the top of the list, files at the bottom
- Show hex of file when selected and A pressed
- Stop screen flickering when changing directory (Note to self: create function that
  uses `\x1b[2J` and then prints empty chars*size of what is on screen) to clear screen
  instead of using the clear screen escape sequence

# Credits
Thanks to [Pirater12](https://github.com/Pirater12) and [LiquidFenrir](https://github.com/LiquidFenrir) for helping me
with the code :)

Icon made by [Madebyoliver](http://www.flaticon.com/authors/madebyoliver) from [www.flaticon.com](http://www.flaticon.com) is licensed by [CC 3.0 BY](http://creativecommons.org/licenses/by/3.0/)

# Notes (mainly for myself)
[Directory stuff](https://www.gnu.org/software/libc/manual/html_node/Directory-Entries.html) | [Using escape codes](https://smealum.github.io/ctrulib/graphics_2printing_2colored-text_2source_2main_8c-example.html#a1) | [Explanation of `strtok()`](http://stackoverflow.com/a/3890186)
