# Dickompiler
A simple decompiler for the Tickflow format found in some Rhythm Heaven games.

Todo
1. Read the binary data from the corpus folder on a per-file 
2. Read the tickflow_definition file to determine what exactly we're searching for (and how to parse it)
3. Examine the binary data to find tickflow code within it
    - Figure out how to recognize what tickflow looks like
4. Convert the tickflow bytecode into (more) readable text
5. Write the resulting text to an output tickflow file

Current Goals
- A better dump command that properly extracts *all* tickflow from a given file. (Since tickompiler misses a lot of things)
- Better formatting and command names (although it'll be syntactically similar to tickflow, not a complete overhaul like tickscript)
- Compilation that can patch the exefs/main.dol/overlays directly

Future Goals
- Multiline Comments (finally!!!)
- Tempo file editing (where this is possible)
- Perhaps baking in some features from rupert's tools 
- Multi-region support
- Rhmpatch and Spicerack support
- Better software support (probably Notepad++, Sublime Text, and Vscode)
- Checking the github repo for updates
- RHRE and HS to Tickflow :cherryhappy:

Docs used:
- [Rhythm Heaven DS Tickflow Docs](https://drive.google.com/drive/folders/1r9Xgks_UII1SPYUGr8fYme8EajWG93bj)
- [Rhythm Heaven Fever Tickflow Docs](https://cdn.discordapp.com/attachments/277545867723145226/1479245528993894430/Rhythm_Heaven_Fever_Docs.zip?ex=6a41a141&is=6a404fc1&hm=7d72afeae860a62a351c19dcf18ffc2f9320f27716a656915e41cec411f6e258&) (Download Link)
- [Rhythm Heaven Megamix Docs Archive](https://rhmodding.github.io/rhm-docs-archive/)