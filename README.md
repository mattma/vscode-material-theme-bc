# VSCode Material Theme

## Build VSCode Theme Package

### VS Code Extensions Manager

```bash
# Install global package `@vscode/vsce`
npm install -g @vscode/vsce

# Init the vscode package project
npx @vscode/vsce init
```

## Find the theme setting

1. Open Command Palette (Ctrl + Shift + P / Cmd + Shift + P on Mac).
2. Choose `Developer: Generate color theme from the current settings`

## Real-Time Theme Customization in VSCode

VSCode provides a way to edit theme colors dynamically using settings.json:

Method 1: Live Edit with workbench.colorCustomizations

1. Open Command Palette (Ctrl + Shift + P / Cmd + Shift + P on Mac).
2. Search for Preferences: Open Settings (JSON) and open it.
3. Add the following snippet to test changes in real-time:


```json
{
  "workbench.colorCustomizations": {
    "sideBar.background": "#1e1e1e", // Change Explorer Sidebar color
    "editor.background": "#252526", // Change Editor Background
    "editor.foreground": "#ffffff" // Change Default Text color
  }
```


## Release and package the theme

It will generate the file `vscode-material-theme-bc-[version].vsix` at the root of the project

```bash
npx @vscode/vsce package
```

Then, open the VSCode, go to `extensions` tab, then click on `...`, the three dots at the top right corner, use `install from VSIX` to load the theme file.
