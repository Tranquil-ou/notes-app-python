# Notes app in Python
Notes application written in Python 3.8 

## Features
- Cross-platform compatibility
- Sections for organizing notes, allowing addition, renaming, and deletion
- Flexibility to store note files locally or in shared cloud folders like DropBox, enabling seamless cross-device synchronization
- Comprehensive search function, supporting both full-text and word-specific queries within individual sections or across all sections
- Personalized font and color options, with the ability to save custom settings
- Automatic saving of note content while typing

## Syncing Notes
- Move the notes file to a folder that supports synchronization across your chosen devices.
- Open the app's file icon menu, select 'choose storage file,' and navigate to the synchronized folder location to establish the connection. Your synchronization setup is now complete.


### Building the application

#### Linux app build from Linux environment:
- Prerequisites example:

```language="sh"
virtualenv venv_notes_app
source bin/activate
(venv_notes_app) python -m pip install --upgrade pip wheel setuptools
(venv_notes_app) python -m pip install PyInstaller
mv notes.spec notes_linux.spec
change in the spec file the line datas=[], to datas=[("notes_app/view/notes_view.kv", "notes_app/view/")],
```

- Build command example:
```language="sh"
(venv_notes_app) pyinstaller notes_linux.spec
```