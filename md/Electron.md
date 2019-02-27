# Electron

### [中文文档](https://electronjs.org/)

electron运用(html,css,js)等web技术构建桌面应用

```js
# 克隆示例项目的仓库 脚手架
git clone https://github.com/electron/electron-quick-start

# 进入这个仓库
$ cd electron-quick-start

# 安装依赖并运行
$ npm install

# 启动
npm start
```
安装完毕之后
- .gitignore(git上传提交时候过滤文件)
- index.html(ele应用页面主入口，前端)
- main.js(控制ele应用的后台文件，后端)
- package.json(记录ele应用的依赖，和启动命令)
- renderer.js(配合index.html使用的了逻辑文件，控制前端的逻辑，去调用nodejs api)

打开之后，会发现是一个app，你要关闭这个app，交互是跟网页版本不一样

### 用生成后的桌面应用 调试开发

1.开启前端或后端服务器
2.electron-quick-start/main.js
```js
  ···
  //直接让start后的调试页面，指向你的服务器
  mainWindow.loadURL('http://localhost:3000/#/hot')

  ···
```
3. npm start

### 生成win和mac系统的安装包

先安装electron-packager

`cnpm i electron-packager -g`

在package.json的scripts中添加命令
```
//package.json

"scripts": {
    "start": "electron .",
    "package:win": "electron-packager . --overwrite --platform=win32 --arch=ia32 --out=out --icon=assets/app-icon/win/app.ico",
    "package:mac": "electron-packager . --overwrite --platform=darwin --arch=x64 --out=out --icon=assets/app-icon/mac/app.icns --osx-sign.identity='Developer ID Application: GitHub' --extend-info=assets/mac/info.plist"
  },
```

在根目录添加文件夹assets <br/>  

`--icon=assets/app-icon/win/app.ico`为图标路径

最后执行`npm run package:win` 进行打包

