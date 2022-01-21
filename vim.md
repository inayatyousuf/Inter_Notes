Name Inayat Yousuf.
Task: VIM   (in terminal type vimtutor to know more about vim and to exit from vimtutor type :q or ZZ or :x )


VIM and its basic commands.
Vim is a free and open-source, screen-based text editor program for Unix. Vim is a highly configurable text editor built to make creating and changing any kind of text very efficient.

Before we go for the commands we first try to understand how vim works it has different modes like – Normal mode, Insert mode, Visual mode, Ex Mode.

1. Normal Mode: Normal Mode is also known as Command Mode, as it's where you're usually entering commands. Commands can be movements, deletions, or commands that do these things and then enter into Insert Mode.

2. Insert Mode: Insert Mode is where you make changes to your file, The way of entering Insert Mode from Normal Mode is simple just by pressing “i” it stands for the insert or “a” stands for append. To go back to normal mode press Esc.

3. Visual Mode: Visual Mode is a way to select text. It's a lot like Normal Mode, except your movements change your highlighting. You can select text both character-wise or line-wise, and once in one of those modes your movements select more text. To enter into this mode from Normal mode just press “v”

4. Ex Mode: is a mode where you get a ":" prompt, and you can enter commands. 

Commands:
Before we start we do not need arrow keys of the keyboard to move the cursor left right top and bottom for that vim provides some special keys.
j: move down one line
k: move up one line
h: move left one character
l: move right one character
If we want to exit from this document then in normal mode type :q! it is for the exit without saving.
But if we want to exit and also save the document changes the type :wq (w for write and q for quit).
If we want to save the document then use :w command it will alert the message the first time and shows no file name for that use :w file1.txt 
We can also move by word:
w: move forward one word
b: move back one word
e: move to the end of your word
Moving by sentence or paragraph:
): move forward one sentence
}: move forward one paragraph
Moving within the screen
H: move to the top of the screen
M: move to the middle of the screen
L: move to the bottom of the screen
gg: go to the top of the file
G: go to the bottom of the file
^F: page down
^B: page up
Copy and Paste

To copy we need to first change the mode, for copying we first need to select the text and then copy, selecting the text is done in Visual mode. In normal mode press “v”.

After we change the mode to Visual we can use HJKL to move the cursor, where ever the cursor moves text is going to select.

Next step is to copy the selected text we cannot use ctrl+c,  but in vim we use “y” means yank or copy. Now our text is copied. Or
yy: yank the current line. For only 1 line copy

Now our last step is to paste it for that use “p” command to paste but in normal mode. Or “:put” in Ex Mode.

Undo and Redo
Like in other text editors vim also provide the functionality to undo and redo the actions.
u: undo your last action.
Ctrl-r: redo the last action

Cut and Paste
In the normal mode press “dd” and then move your cursor pointer where ever you want to paste it and press “p” or “:put”

“dd”  is used for deleting only 1 line but if we want to delete multiple lines move your cursor where from you want to delete and mention how many lines you want to delete. Eg

“4dd”  delete the 4 lines 
If we want to delete the character then use “x”, if multiple characters then use the number of characters you want to delete before “x” like 3x or 4x etc.

To delete full word user “dw” for multiple words use “4dw” or “6dw”.

Navigate in the page:

In normal mode, if you want to go top of the document press “gg” and for the bottom press “shift + g” or “G”.
If we want to go to the specific line number then press “lineNumbergg” eg 5gg.


Searching the particular word in a document:

If we want to search a word in the document then use “/” and then searching word.
Eg in normal mode type    /possible
If we want to see where is our next searched word exists in our document then simply press the “n” keyword.

Sometimes we want to search the word from the bottom then at that time use “?” instead of “/”.

Searching and Replacing:

Searching and replacing is used to search the word and replace that word with some other word.
If we want to change all words then use “ :%s/searchedword/replacedword  ”
Eg  :%s/inayat/zahid — this command changes the all inayat word into zahid.

But sometimes we want to conform before replacing – for that use “%s/inayat/zahid/c” when we hit the enter it does not replace it shows us the whether you want to replace or not or you want to quit.
For replacing press y 
For no replace press n
For quit press q


Multiple files:

If we want to work with multiple files then we simply use the split command.

In normal mode – :split newfileName    or :split file3.txt
It splits the window horizontally and we can move our cursor from one file to another by “ctrl + w”

We can also split the files vertically for that type “v” before split like :vsplit file3.txt


Motion command reference
j: move down one line
k: move up one line
h: move left one character
l: move right one character
0: move to the beginning of the line
$: move to the end of the line
w: move forward one word
b: move back one word
e: move to the end of your word
): move forward one sentence
}: move forward one paragraph
:line_number: move to a given line number
H: move to the top of the screen
M: move to the middle of the screen
L: move to the bottom of the screen
^E: scroll up one line
^Y: scroll down one line
gg: go to the top of the file
G: go to the bottom of the file
^U: move up half a page
^D: move down half a page
^F: move down a page
^B: move up a page
Ctrl-i: jump to your previous navigation location
Ctrl-o: jump back to where you were.
i: insert before the cursor
a: append after the cursor
I: insert at the beginning of the line
A: append at the end of the line
o: open a new line below the current one
O: open a new line above the current one
r: replace the one character under your cursor
R: replace the character under your cursor, but just keep typing afterward
cm: change whatever you define as a movement, e.g. a word, or a sentence, or a paragraph.
C: change the current line from where you're at
ct?: change up to the question mark
s: substitute from where you are to the next command (noun)
S: substitute the entire current line
x: exterminate (delete) the character under the cursor
X: exterminate (delete) the character before the cursor
dm: delete whatever you define as a movement, e.g. a word, or a sentence, or a paragraph.
dd: delete the current line
dt.: delete from where you are to the period
D: delete to the end of the line
J: join the current line with the next one (delete what's between).


