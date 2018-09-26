## electron desktop idle

Node/Electron module to detect idle desktop users (OSX, Windows and Linux). Adapted to use with webpack.

**Stable | Actively maintained | Pull Requests Welcome**

_Forked from [bithavoc/node-desktop-idle](https://github.com/bithavoc/node-desktop-idle)_

### Installation
```
npm install --save desktop-idle
# or yarn
yarn add desktop-idle
```

### Cross-Platform Support
* **Windows:** [GetLastInputInfo](https://msdn.microsoft.com/en-us/library/windows/desktop/ms646302(v=vs.85).aspx), see `src/win/idle.cc`.
* **Mac(OSX):** [CoreGraphics Event Source](https://developer.apple.com/documentation/coregraphics/1408790-cgeventsourcesecondssincelasteve), see `src/mac/idle.cc`.
* **Linux:** [X Screensaver](https://linux.die.net/man/3/xscreensaverqueryinfo), see `src/linux/idle.cc`.

### Usage
```
var desktopIdle = require('desktop-idle');
console.log(desktopIdle.getIdleTime());
```

### Linux Requirements

X server development package and pkg-config are required:

`apt install libxss-dev pkg-config`

### Test

```
yarn test
```