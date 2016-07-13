# [](#electron)electron

## [](#executing-js-in-a-browserwindow)Executing js in a BrowserWindow

### [](#with-executejavascript)with `executeJavaScript`

If you just want to run js in a page there is <http://electron.atom.io/docs/api/web-contents/#webcontentsexecutejavascriptcode-usergesture-callback>

However if you want to read some information or get a result you need to use `ipc`. Example here of using `ipc` with `executeJavaScript` together: <https://discuss.atom.io/t/how-to-return-value-from-webcontents-executejavascript/22726/9>

There's a small helper module for this too: <https://github.com/joshwnj/electron-run-in-browser>

### [](#with-a-preload-script)with a `preload` script

When creating a `BrowserWindow` you can specify a js file in the `webPreferences.preload` option: <http://electron.atom.io/docs/api/browser-window/>

This file is run before any js, and has access to the electron API so you can set up communication over `ipc`.
