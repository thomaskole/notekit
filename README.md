# NoteKit
This program is a structured notetaking application based on GTK+ 3. Write your notes in instantly-formatted Markdown, organise them in a tree of folders that can be instantly navigated from within the program, and add hand-drawn notes by mouse, touchscreen or digitiser.

## Why?
I figured it would be nice to have a free-software, platform-independent OneNote. While there is a remarkable number of free (speech or beer) notetaking applications out there, to my best knowledge, none of them simultaneously check the following boxes:

* note organisation
* text as a first-class object
* formatting
* simple, standard on-disk format
* tablet input

## How to build
Either invoke `make`, or get [CodeLite](https://codelite.org/), open and build the workspace.

Required libraries:

* `libgtkmm-3.0-dev`>=3.20 (UI stuff)
* `libgtksourceviewmm-3.0-dev`>=3.18 (more UI stuff)
* `libjsoncpp-dev` ~ 1.7.4 (config files; older versions may work)
* `zlib1g-dev`

Nothing about this has been tested on other platforms than X11-based Linux.
## Usage notes
* Notes are saved in `notesbase/` relative to the binary path. (This will be made configurable eventually.)
* To create a new note, doubleclick a `+` node in the tree view and enter a name.
* To create a new folder, doubleclick a `+` node in the tree view and enter a name ending in `/`, e.g. `new folder/`.
* To edit the default colour palette, right-click a colour picker.
* Drawings can currently only be deleted whole. (This will be fixed eventually.)
* Files are saved automatically when the window is closed, or when a different file is opened.
* The document formatting is mostly based on standard `GtkSourceView` language and style files. If you want to change colours or syntax highlighting rules, you can edit them in the `sourceview/` subfolder.
* The program loads a custom Gtk+ stylesheet found in `data/stylesheet.css`. Clear it if parts of the UI look wonky.

## Project status
Late alpha. Creating and editing notes and drawing works well enough, but many basic quality-of-life features (such as an eraser tool) are still missing.

## Planned features
* An eraser tool.
* Selecting strokes, moving and transforming selections, etc.
* Floating figures (so drawings can exist on top of text rather than as blocks that text floats around).
* LaTeX math using `lasem`.
* More Markdown rendering, e.g. actually formatting links, and turning `- [ ]` syntax into real checkboxes.
