# Editor (markdown and code editorm, CodeMirror, etc.) settings

The default behaviour in the code and markdown cell editors has some annoying foibles. For example, barckaets aren't necessarily closed, highlighting text and clickig an open bracket deletes the text rather than wrapping it in brackets, etc.)

The following settings are recommneded:

- in `.jupyter/lab/user-settings/@jupyterlab/codemirror-extension/plugin.jupyterlab-settings`:

```json
{
    "defaultConfig": {
        "autoClosingBrackets": true,
        "codeFolding": false,
        "highlightActiveLine": false
    }
}
```

- in `.jupyter/lab/user-settings/@jupyterlab/fileditor-extension/plugin.jupyterlab-settings`:

```json
{
    "editorConfig": {
        "autoClosingBrackets": true,
        "codeFolding": false
    }
}
```

- in `.jupyter/lab/user-settings/@jupyterlab/notebook-extension/tracker.jupyterlab-settings`:

```json
{
    "codeCellConfig": {
        "autoClosingBrackets": true,
        "lineNumbers": false,
        "lineWrap": false
    },
    "defaultCell": "code",
    "markdownCellConfig": {
        "lineNumbers": false,
        "matchBrackets": true
    }
}
```
