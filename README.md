# jb:// url handler

This is a script to handle the "jb://" url scheme.  
This scheme is completely unofficial, and is made just for my convenience.  
It is used to open specified JetBrains IDE, on a specified project, on a specified file.

## Url examples

With absolute file path, and using "~":
```
jb://localhost?api=v1&ide=writerside&project_path=~/Documents/MediaWiki/&file_path=~/Documents/MediaWiki/wiki.blender.org/Building_Blender/Linux/Arch/Arch.mw
```

With file path relative to project root:
```
jb://localhost?api=v1&ide=writerside&project_path=~/Documents/MediaWiki/&file_path=wiki.blender.org/Building_Blender/Linux/Arch/Arch.mw
```

## How it works

It just runs the IDE with the parameters. 

From the `--help` of the ide:
```
/project/dir
  opens a project from the given directory
[/project/dir|--temp-project] [--wait] [--line <line>] [--column <column>] file
  opens the file, either in a context of the given project or as a temporary single-file project,
  optionally waiting until the editor tab is closed
```

## Installation

If using Arch Linux, you can install [jb-url-handler](https://aur.archlinux.org/packages/jb-url-handler) from AUR.
