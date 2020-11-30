# Ionic, Capacitor, Angular 应用构建 Starter

## 命令

## 建立 Ionic 项目

- `ionic start ionic-cap-ng-app-starter blank --type=angular --capacitor`

## 安装依赖

- `npm i ngx-electron @capacitor-community/electron electron`

> 这里同时安装了 Capacitor 社区版与官方的 `electron`，是因为 Capacitor 要求使用社区版，而 `ngx-electron` 以来官方的 `electron`。

## 修改根目录下的 `package.json`

在 `scripts` 下，加入 `"electron:start": "ionic build && npx cap copy && npx cap open @capacitor-community/electron"` 启动脚本。

## 修改 `electron/package.json`

加入 `dist:win` 与 `dist:linux`，实现应用自动化构建。

## 使用方法

1. 克隆到本地

`git clone git@github.com:gnu4cn/ionic-cap-ng-app-starter`

2. 运行 `npm init`、`ionic init`

3. 删除 `.git` 目录，运行 `git init` 并添加自己的 Git 代码仓库
