```json
// Coloque as suas associações de teclas neste arquivo para substituir os padrõesauto[]
[
  {
    "key": "ctrl+shift+s",
    "command": "workbench.action.files.saveFiles"
  },
  {
    "key": "ctrl+shift+k",
    "command": "-editor.action.deleteLines",
    "when": "textInputFocus && !editorReadonly"
  },
  {
    "key": "ctrl+n",
    "command": "welcome.showNewFileEntries"
  },
  {
    "key": "ctrl+alt+win+n",
    "command": "-welcome.showNewFileEntries"
  },
  {
    "key": "ctrl+n",
    "command": "explorer.newFile"
  },
  {
    "key": "ctrl+shift+w",
    "command": "workbench.action.closeAllEditors"
  },
  {
    "key": "ctrl+k ctrl+w",
    "command": "-workbench.action.closeAllEditors"
  },
  {
    "key": "ctrl+shift+w",
    "command": "-workbench.action.closeWindow"
  },
  {
    "key": "ctrl+shift+o",
    "command": "outline.focus"
  },
  {
    "key": "ctrl+q",
    "command": "editor.action.deleteLines"
  },
  {
    "key": "ctrl+1",
    "command": "workbench.action.terminal.clear"
  },
  {
    "key": "ctrl+l",
    "command": "workbench.action.gotoLine"
  },
  {
    "key": "ctrl+g",
    "command": "-workbench.action.gotoLine"
  },
  {
    "key": "shift+alt+g",
    "command": "references-view.showCallHierarchy",
    "when": "editorHasCallHierarchyProvider"
  },
  {
    "key": "shift+alt+h",
    "command": "-references-view.showCallHierarchy",
    "when": "editorHasCallHierarchyProvider"
  },
  {
    "key": "ctrl+o",
    "command": "workbench.action.gotoSymbol"
  },
  {
    "key": "ctrl+shift+o",
    "command": "-workbench.action.gotoSymbol"
  },
  {
    "key": "f8",
    "command": "-editor.action.marker.nextInFiles",
    "when": "editorFocus"
  },
  {
    "key": "f8",
    "command": "workbench.action.debug.continue",
    "when": "debugState == 'stopped'"
  },
  {
    "key": "f5",
    "command": "-workbench.action.debug.continue",
    "when": "debugState == 'stopped'"
  },
  {
    "key": "f8",
    "command": "workbench.action.debug.start",
    "when": "debuggersAvailable && debugState == 'inactive'"
  },
  {
    "key": "f5",
    "command": "-workbench.action.debug.start",
    "when": "debuggersAvailable && debugState == 'inactive'"
  },
  {
    "key": "f6",
    "command": "workbench.action.debug.stepOver",
    "when": "debugState == 'stopped'"
  },
  {
    "key": "f10",
    "command": "-workbench.action.debug.stepOver",
    "when": "debugState == 'stopped'"
  },
  {
    "key": "f5",
    "command": "workbench.action.debug.stepInto",
    "when": "debugState != 'inactive'"
  },
  {
    "key": "f11",
    "command": "-workbench.action.debug.stepInto",
    "when": "debugState != 'inactive'"
  },
  {
    "key": "f8",
    "command": "workbench.action.debug.pause",
    "when": "debugState == 'running'"
  },
  {
    "key": "f6",
    "command": "-workbench.action.debug.pause",
    "when": "debugState == 'running'"
  },
  {
    "key": "ctrl+3",
    "command": "editor.action.sourceAction",
    "when": "editorTextFocus && !editorReadonly && editorLangId == 'java'"
  },
  {
    "key": "ctrl+4",
    "command": "editor.action.refactor",
    "when": "editorHasCodeActionsProvider && textInputFocus && !editorReadonly"
  },
  {
    "key": "ctrl+shift+r",
    "command": "-editor.action.refactor",
    "when": "editorHasCodeActionsProvider && textInputFocus && !editorReadonly"
  },
  {
    "key": "ctrl+m",
    "command": "explorer.newFolder"
  },
]

```
