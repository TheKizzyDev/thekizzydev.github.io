+++
title = 'Setting up GDScript Formatter in VSCode under Windows 11'
date = 2024-02-22T22:19:08-08:00
draft = false
+++
1. Install [python 3.12+](https://apps.microsoft.com/detail/9ncvdn91xzqp?hl=en-gm&gl=GM).
2. Install python-setuptools. In Windows Powershell, run:
   `pip install setuptools`
3. Install [gdtoolkit](https://github.com/Scony/godot-gdscript-toolkit) in Windows Powershell by running:
   `pip install "gdtoolkit==4.*"`
   
   If using Godot 3.\*, run:
   `pip install "gdtoolkit==3.*"`
4. Install [vscode](https://code.visualstudio.com/download).
5. Go to **View > Extensions**. Install the following:
   - [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
   - [GDScript Formatter by Razoric](https://marketplace.visualstudio.com/items?itemName=Razoric.gdscript-toolkit-formatter)
8. Open the settings.json by pressing, **Ctrl + Shift + P**, and typing **Open User Settings**.
9. Click on, **Preferences: Open User Settings (JSON)**.
10. Add the following entries:
```json
{
	// ...other entries. Make sure there's a comma after these entries.
    "[gdscript]": {
        "editor.defaultFormatter": "Razoric.gdscript-toolkit-formatter"
        },
	"editor.formatOnSave": true
}
```
11. The formatter is now setup.