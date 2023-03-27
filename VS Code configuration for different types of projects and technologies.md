# VS Code configuration for different types of projects and technologies

## Frontend development (html + css)

### VS Code extensions

- Auto Renema Tag

- Better Comments

- Community Material Theme

- Live Server

- Prettier

- Tailwind CSS IntelliSense

No need to comment any of these extensions ;)

### My VS Code settings

All of my enviroment setting are stored per project in the `.vscode` folder. And here they are .. so far:

```json
{
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.fontSize": 16,
    "editor.formatOnPaste": true,
    "editor.formatOnSave": true,
    "editor.wordWrapColumn": 999999,
    "editor.mouseWheelZoom": true,
    "editor.smoothScrolling": true,
    "editor.cursorSmoothCaretAnimation": "on",
    "editor.stickyScroll.enabled": true,
    "explorer.compactFolders": true,
    "workbench.list.smoothScrolling": true,
    "terminal.integrated.smoothScrolling": true,

    "prettier.useTabs": true,
    "prettier.tabWidth": 4,
    "prettier.endOfLine": "crlf",
    "prettier.singleAttributePerLine": false,
    "prettier.bracketSameLine": true,
    "prettier.trailingComma": "es5",
    "prettier.useEditorConfig": false,
    "prettier.semi": false,

    "liveServer.settings.root": "/public",
    "liveServer.settings.port": 5500,
    "editor.tokenColorCustomizations": {
        "comments": "#aaaaaa"
    }
}
```

## Laravel
