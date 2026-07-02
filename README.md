# Dickompiler
A simple decompiler for the Tickflow format found in some Rhythm Heaven games.

Todo
- Decompile command
	- Read the Tickflow data from the corpus folder on a per-file basis
	- Parse the Tickflow data and output it to a file as readable .tickflow text 
- Compile command
	- Remove all the comments from the .tickflow file (both single line and multi line)
	- 

3. Patch the .tickflow files back into the game's binaries

Future Goals
- Replacing or expanding #index to be more like .org
- Tempo file editing (where this is possible)
- Perhaps baking in some features from rupert's tools 
- Multi-region support for DS, Fever, and Megamix
- Rhmpatch and Spicerack Compilation support
- Better software support (probably Notepad++, Sublime Text, and Vscode)
- Checking the github repo for updates
- RHRE and HS to Tickflow :cherryhappy:

```
Tickflow Command - 4 bytes (or 32 bits)

In bits
ZZZZ ZZZZ ZZZZ ZZZZ ZZYY YYXX XXXX XXXX

X - Opcode
Y - Number of word args (4 bytes per word)
Z - Immediate Argument
```