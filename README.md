# electron-sendbird

1) Get your account at https://www.sendbird.com 
2) From your Dashboard, create a group channel and get the URL
3) Run this demo and enter you information:

![Sendbird](https://github.com/warodri-sendbird/electron-sendbird/blob/main/Screenshot%202021-03-04%20at%2017.40.57.png?raw=true)

## Run this demo

Run with ```npm start```

## Build 

Install Electron packager for your project:
```npm install electron-packager --save-d```

Install Electron packager globally:
```npm install electron-packager -g```

Make sure you have a product name in your package.json:
```
{
   "name": "electron-sendbird",
   "productName": "Electron Sendbird",
   "version": "0.1.0",
   "main": "main.js",
   "devDependencies": {
     "electron": "^1.4.3",
     "electron-packager": "^8.1.0"
   }
}
```

Build for Mac:
```electron-packager . --overwrite --platform=darwin --arch=x64 --icon=assets/icons/mac/icon.icns --prune=true --out=release-builds```

Build for Windows:
```electron-packager . electron-tutorial-app --overwrite --asar=true --platform=win32 --arch=ia32 --icon=assets/icons/win/icon.ico --prune=true --out=release-builds --version-string.CompanyName=CE --version-string.FileDescription=CE --version-string.ProductName="Electron Sendbird"```

Build for Linux:
```electron-packager . electron-tutorial-app --overwrite --asar=true --platform=linux --arch=x64 --icon=assets/icons/png/1024x1024.png --prune=true --out=release-builds```

