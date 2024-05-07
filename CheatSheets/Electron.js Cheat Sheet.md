## Introduction to Electron.js

Electron.js is an open-source framework developed by GitHub for building cross-platform desktop applications using web technologies like HTML, CSS, and JavaScript.

## Getting Started

1. **Installation:**
   - Install Node.js and npm.
   - Initialize your project: `npm init`.
   - Install Electron.js: `npm install electron`.

2. **Project Structure:**
   - Main Process: `main.js`.
   - Renderer Process: HTML, CSS, JavaScript files.
   - Package.json: Define entry points and dependencies.

## Basics

### Main Process

```javascript
// main.js

const { app, BrowserWindow } = require('electron');

app.on('ready', () => {
  let mainWindow = new BrowserWindow({ width: 800, height: 600 });
  mainWindow.loadFile('index.html');
});
```

### Renderer Process

```html
<!-- index.html -->

<!DOCTYPE html>
<html>
<head>
  <title>My Electron App</title>
</head>
<body>
  <h1>Hello Electron!</h1>
</body>
</html>
```

### Inter-Process Communication (IPC)

```javascript
// main.js

const { ipcMain } = require('electron');

ipcMain.on('ping', (event, message) => {
  console.log(message); // Prints: "Hello from Renderer"
  event.sender.send('pong', 'Hello from Main');
});
```

```javascript
// renderer.js

const { ipcRenderer } = require('electron');

ipcRenderer.send('ping', 'Hello from Renderer');

ipcRenderer.on('pong', (event, message) => {
  console.log(message); // Prints: "Hello from Main"
});
```

## Advanced Features

1. **Native APIs:** Access system resources using Node.js modules.
2. **Menus and Dialogs:** Create custom menus and dialogs for your app.
3. **File System Access:** Read/write files using Node.js fs module.
4. **Multi-Window Support:** Create multiple windows for your application.
5. **Packaging and Distribution:** Package your Electron app for distribution.

## Debugging and Tools

1. **DevTools:** Toggle Developer Tools for debugging.
2. **Electron Forge:** Automate packaging and distribution.
3. **Electron Builder:** Build installers for your app.

## Best Practices

1. **Performance Optimization:** Minimize memory usage and optimize rendering.
2. **Security:** Handle user data securely and update dependencies regularly.
3. **Cross-Platform Compatibility:** Test your app on different operating systems.

## Resources

- Official Documentation: [Electron.js Docs](https://www.electronjs.org/docs)
- Community Forums: [Electron Forum](https://discuss.atom.io/c/electron)
- Sample Projects: [Electron Samples](https://github.com/electron/electron-api-demos)

This cheat sheet covers the basics, advanced features, debugging tools, best practices, and additional resources for Electron.js development. Feel free to refer to the official documentation for more detailed information on specific topics.