<p align="center">
  <img src="https://img.shields.io/github/v/release/evsar3/sshfs-win-manager?sort=semver">
  <img src="https://img.shields.io/github/downloads/evsar3/sshfs-win-manager/total">
  <img src="https://img.shields.io/github/issues-raw/evsar3/sshfs-win-manager/bug?color=red">
  <a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=HXZUJ8WX47238" style="margin-left: 50px; vertical-align: middle;">
    <img src="https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif" alt="Donate" title="PayPal - The safer, easier way to pay online!">
  </a>
</p>

# SSHFS-Win Manager

## ✨ This is a fork of `SSHFS-Win Manager 1.3.1`

### New Features

* Add an option to mount as a Network Drive instead of Local Drive
  * Learned it from [here](https://github.com/winfsp/sshfs-win/issues/125#issuecomment-555150176)
  * Windows Registry will be modified to correctly display the Network Drive's name (instead of the UNC path). 
    * Check `HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\MountPoints2\` to see what will be added
    * Learned it from [here](https://github.com/winfsp/sshfs-win/issues/46)

### Build Notes

* All deps are too old, I had struggled to migrate it but it's of too much work and I gived up :(
* New versions of node (>=17) will fail as the old `terser` plugin use some deprecated crypto algrithms. **Node 16** works for me, I recommand use [nvm-windows](https://github.com/coreybutler/nvm-windows/releases) to insteall it
* `node-sass` install failed for me, so I upgrade it to `^7`
* using `pnpm` with `shamefully-hoist=true` can start dev but failed build, `npm` works

### Build Instructions

1. Install [nvm-windows](https://github.com/coreybutler/nvm-windows/releases)
2. `nvm install 16; nvm use 16;`
3. `npm install`
4. `npm build`

---

## Introduction 
SSHFS-Win Manager is a GUI (graphics user interface) for SSHFS on Windows (comming soon for other platforms).

## Installation
**Step 1**  

Install SSHFS-Win on your Windows computer.  
Follow they [installation instructions](https://github.com/billziss-gh/sshfs-win/blob/master/README.md) before continue.  

**Step 2**  

Once SSHFS-Win is installed, [**download the lastest setup**](https://github.com/evsar3/sshfs-win-manager/releases/latest) from the [releases](https://github.com/evsar3/sshfs-win-manager/releases) section and install it.  

**Step 3**  

Add your connections and enjoy!

## Features

- Electron-based application. [Electron](https://github.com/electron/electron) is the same engine that powers [Visual Studio Code](https://github.com/microsoft/vscode), [Discord](https://discordapp.com/), [GitKraken](https://www.gitkraken.com/) and [many more](https://www.electronjs.org/apps).

- User-friendly and intuitive interface

- Multiple authentication methods: 
  - Password<sup>1</sup>
  - Private Key (without password)
  - Ask for password

- Startup with Windows
- Close to system tray
- Quick debug tool
- Supports advanced command line params
- Easily duplicate connections
- Reorder connections
- Connection debug log

## Screenshots
![Main Window](https://user-images.githubusercontent.com/1992754/179056109-a0df5872-f187-40b1-895c-9ef57abd5fe7.png)  
*Main Window*

![Add Connection](https://user-images.githubusercontent.com/1992754/179056126-0f767346-fe93-48fc-9ceb-3514b0b7b386.png)  
*Add & edit connections*

![Open mounted drive](https://user-images.githubusercontent.com/1992754/179056142-3d368a65-f9c6-4232-86d6-bb8db6eff556.png)  
*Explore mounted drive*

![System tray](https://user-images.githubusercontent.com/1992754/179056152-9a7088c4-f23a-4c0d-b70b-1ccf879897fb.png)  
*Close to system tray*

## Bugs & help
If you have any question or a bug report please open a [new issue](https://github.com/evsar3/sshfs-win-manager/issues/new)

## Contributing
If you want to contribute with this project, please see the [contributing guide-lines](https://github.com/evsar3/sshfs-win-manager/blob/master/CONTRIBUTING.md)  
If you just want to build or compile this project see instructions [here](https://github.com/evsar3/sshfs-win-manager/blob/master/CONTRIBUTING.md#building-and-compiling)

## Donation
If you like this project, please consider [making a donation](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=HXZUJ8WX47238). 100% of the founds will be revert for <u>charity</u>.

## Notes
<sup>1</sup> This software stores your password in a plain json file. If there is any concerns on storing your password that way, please use one of the other authentication methods. See issue #28

## License
MIT License

Copyright (c) 2020 Evandro Araújo

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
