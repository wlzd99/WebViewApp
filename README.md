# WebView 套壳 App

纯 WebView 安卓应用，用于加载指定网页。

## 功能

- 全屏 WebView 访问 http://117.80.228.234:8019/index.html
- 支持平板横竖屏自适应
- 支持网页内返回（按返回键回退页面，不是退出 App）
- 开启 JavaScript、LocalStorage 支持
- 支持 HTTP 明文传输（适配内网地址）

## 如何获取 APK（无需 Android Studio）

### 方式一：GitHub Actions 自动构建（推荐）

1. **Fork 或上传本项目到你的 GitHub 仓库**
2. 进入仓库的 **Actions** 标签页
3. 点击左侧 **"Build APK"** -> **Run workflow**
4. 等待约 3-5 分钟构建完成
5. 进入最新完成的 Workflow，在 **Artifacts** 区域下载 `release-apk.zip`
6. 解压得到 `app-release-unsigned.apk`，可直接安装到安卓平板

### 方式二：找有 Android Studio 的同事帮忙

把本项目文件夹给他，用 Android Studio 打开，点击 **Build > Build Bundle(s) / APK(s) > Build APK(s)** 即可。

## 安装到平板

1. 把 APK 文件传到安卓平板（微信、QQ、USB 均可）
2. 在文件管理器中点击 APK 安装
3. 如提示"未知来源"，请允许安装未知应用

## 修改加载的网址

编辑 `app/src/main/java/com/example/webviewapp/MainActivity.java` 中的 `TARGET_URL` 常量即可。

## 技术说明

- minSdk: 24（Android 7.0）
- targetSdk: 34
- 使用原生 Android WebView，无第三方框架
