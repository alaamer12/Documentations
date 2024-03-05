## Building Websites

### Desktop
- To build websites into binary files, you would usually use `npx electron-packager . --platform=win32 --arch=x64 --icon=icon.ico`.
  - **Note:** This command builds for Windows. I haven't tried it for Linux or Mac.
- To test how it would look, you would usually use `electron .` or `npx electron .`.

### Mobile
- I haven't tried building for mobile before, so I don't have any knowledge about it. Shall I leave some resources for the future?
  - Common tools: Ionic, Cordova, Capacitor, etc.

### Other
- Usually, you would use `gulpjs` to help in the distribution processes of websites, which would involve minification, parsing, renaming, etc.
  - Also, `tsc` can be used if using pure TypeScript, but `gulpjs` can do it as well.

## Python

### Desktop
- Usually, you would use the third-party service `pyinstaller` with a command similar to `pyinstaller --onefile main.py`.
  - There are other libraries, but I think this is the best. Also, I have not tested the other libraries.
  - PyInstaller is capable of distributing to different binary formats.

### Mobile
- In years past, there were two options only: BeeWare and Kivy. I think both of them use `buildozer` as the bundler to bundle it to machine code.
  - We tried to make applications with both of them, but we failed because of a bug we encountered when we used buildozer. Now we know the bug and I think we can easily fix it.
  - Now there is a new technology called `Flet`, which is a wrapper about Flutter to make desktop and mobile applications with the same source code with your favorite language, but it is only supporting Python at the moment and is in beta state. So, we won't talk further until it reaches the stable state.
### Package
- You can package python project into `PyPi` by
 - `pip install setuptools wheel`
 - then
 - config the setup in setup.py in the root
 - then
 - `python setup.py sdist bdist_wheel`
 - it will create two directories [build, dist]
 - the package would be in `dist` archived as .tar file
## C++/C#/C
### Desktop
- Actually, I don't know how to build them manually. The only way I know is to build them through Visual Studio.

### Mobile
- You can build mobile applications easily and rapidly in C# with Visual Code, but it is more complex when it comes to C++ or C. Actually, I still don't know if it is straightforward now or not, but as I remember, it is not straightforward.

## React Native [Expo]
### Desktop
- It is possible to distribute it to the desktop, but I haven't tried, and I don't think I will because it is a complex process.

### Mobile
- I haven't used React Native, but I have used Expo a lot. There are two ways to build applications with Expo:
  - With Expo command [locally]: `expo build --profile production --platform android`
  - With eas command [remotely]: `eas build --profile production --platform android`
- You can also choose the profile you want.

### Website
- You can also build websites with React Native and Expo. The command is `expo export`, but you have to make some configurations first.
