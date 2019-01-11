# The vi Editor

Operating the vi editor takes some practice. For many, it is the preferred editor, partly because it is available on any UNIX-like operating system and is included in default Linux installations. Also, if nothing else works, vi will. The short instructions that follow should enable you to edit various configuration files and other types of files with vi.

vi provides three operating modes. 
1. <b>command mode</b> keys are interpreted as command elements. 
2. <b>insert mode</b> interprets all keys as text entries and 
3. <b>last line mode</b> is used for more complex commands, which are entered in the last line.

The most important commands in command mode are:

COMMAND | DESCRIPTOR
-------------- | --------------
ESC | Changes to last line mode.
i | Changes to insert mode (characters appear at the current cursor position).
a | Changes to insert mode (characters appear after the current cursor position).
A | Changes to insert mode (characters are added at the end of the line).
R | Changes to command mode (overwrites the old text).
r | Changes to insert mode and overwrites each character.
s | Changes to insert mode (the character where the cursor is positioned is replaced by the next entry you make).
C | Changes to insert mode (the rest of the line is replaced by the new text).
o | Changes to insert mode (a new line is inserted following the current one).
O | Changes to insert mode (a new line is inserted preceding the current one).
x | Deletes the current character.
dd | Deletes the current line.
dw | Deletes up to the end of the current word.
cw | Changes to insert mode (the rest of the current word is overwritten by the next entries you make).
u | Undoes the last command.
J | Joins the following line with the current one.
. | Repeats the last command.
: | Changes to last line mode.

Each command can be preceded by a number specifying on how many objects the following command should operate. 

Delete three words at once by entering 3dw. 

The command 10x deletes ten characters after the cursor position and 20dd deletes twenty lines.

The most important commands in last line mode are:

COMMAND | DESCRIPTOR
-------------- | --------------
:q! | exits vi without saving any changes
:w filename | saves as filename
:x | saves the modified file and exits the editor
:e filename | edits (loads) filename
:u | undoes the last edit command
