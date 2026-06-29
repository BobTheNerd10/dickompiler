# Dickompiler
A simple decompiler for the Tickflow format found in some Rhythm Heaven games.

Todo
1. Read the Tickflow data from the corpus folder on a per-file basis
2. Parse the tickflow data as readable .tickflow text 
3. Write the resulting text to an output tickflow file
4. Patch the .tickflow files back into the game's binaries

Future Goals
- Multiline Comments (finally!!!)
- Replacing or expanding #index to be more like .org
- Tempo file editing (where this is possible)
- Perhaps baking in some features from rupert's tools 
- Multi-region support for DS, Fever, and Megamix
- Rhmpatch and Spicerack Compilation support
- Better software support (probably Notepad++, Sublime Text, and Vscode)
- Checking the github repo for updates
- RHRE and HS to Tickflow :cherryhappy:

Docs used:
- [Rhythm Heaven DS Tickflow Docs](https://drive.google.com/drive/folders/1r9Xgks_UII1SPYUGr8fYme8EajWG93bj)
- [Rhythm Heaven Fever Tickflow Docs](https://cdn.discordapp.com/attachments/277545867723145226/1479245528993894430/Rhythm_Heaven_Fever_Docs.zip?ex=6a41a141&is=6a404fc1&hm=7d72afeae860a62a351c19dcf18ffc2f9320f27716a656915e41cec411f6e258&) (Download Link)
- [Rhythm Heaven Megamix Docs Archive](https://rhmodding.github.io/rhm-docs-archive/)

```
command arg - 4 bytes

ZZZZ ZZZZ ZZZZ ZZZZ ZZYY YYXX XXXX XXXX

X - opcode
Y - number of args, excluding special/arg0
Z - arg0

arguments - 4 bytes (1 word) each

---------------------------------
example:

0x100<2> 1

opcode: 0x100 = 01 0000 0000 base 2
number of args: 1 = 00 01 base 2
arg0: 2 = 0000 0000 0000 0000 10 base 2
args:
    * 1 = 00 00 00 01 base 16

word 1: 0000 0000 0000 0000 1000 0101 0000 0000 base 2
word 2: 0x00000001
final bytecode: 00008500 00000001

not sure if LE switches up the order, but if so I'd assume it's:
00850000 01000000
altho the first word might be unchanged idk
```