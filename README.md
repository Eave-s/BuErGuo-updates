# BuErGuo 更新仓库

此仓库只用于分发“不贰过”（Android 学习 / 错题复习应用）的**正式版更新制品**，不包含应用源码、数据库、测试材料、日志或签名凭据。

## 当前版本

- 版本：**1.15.3**
- versionCode：**62**
- 包名：`com.buerguo.study`
- APK：`releases/BuErGuo-1.15.3-release.apk`
- SHA-256：`1cda65d6fd32fda70123812b77ad48eb0c02144c42a03ce784ef8a1a147e0003`
- 签名证书 SHA-256：`686575a772aeb2f9dbc51b2e2e4c132939baf641cae6c12e73a1c1402c13a083`
- 数据结构：**v19**（与 1.15.2 相同，可直接覆盖安装）

本版更新内容（修复分屏时悬浮窗被关在本应用那一半、气泡贴边与窗口尺寸保持、新增悬浮窗诊断行）
见根目录 `version.json` 的 `changelog`，或在仓库右侧 **Releases** 页查看。

## 应用内更新怎么工作

应用只从本仓库（GitHub Raw 原站）下载安装包，不使用任何第三方镜像：

1. 读取根目录 `version.json`；
2. 比对 `versionCode`（**比本机大**才提示更新），下载 `apkUrl`；
3. 校验 SHA-256、包名与 APK 内的 versionCode，通过后交给 Android 系统弹安装确认。

## 发布者注意（维护本仓库时）

- **先上传并校验 APK，再改 `version.json`**：顺序反了客户端会拿到 404 或旧包。
- `versionCode` 必须**严格递增**：Android 只认它，回退会让覆盖安装被系统拒绝。
- 只发布 release 签名包（debug 包不进入本仓库），签名证书与包名不得变更。
- 本仓库只放 APK、`version.json` 与说明，不放源码、测试数据、日志、数据库或任何凭据。

## 历史版本

| 版本 | versionCode | APK | 备注 |
| --- | --- | --- | --- |
| 1.15.3 | 62 | `releases/BuErGuo-1.15.3-release.apk` | **当前版本**：修复分屏时悬浮窗被关在本应用那一半（“空气墙”）+ 气泡贴边/窗口尺寸保持 + 悬浮窗诊断行（DB v19） |
| 1.15.2 | 61 | `releases/BuErGuo-1.15.2-release.apk` | 修复跨设备同步漏作答图 + 第一次同步即带图 + 同步边界加固（DB v19） |
| 1.15.1 | 60 | `releases/BuErGuo-1.15.1-release.apk` | 学习草稿自动保存/跨设备续答 + 待录入任务同步 + 新题每日配额修复 |
| 1.14.9 | 58 | `releases/BuErGuo-1.14.9-release.apk` | 全局悬浮窗 + 新气泡交互 + 公式/输入法/文件修复 + 详情页上下文 |
| 1.13.0 | 46 | `releases/BuErGuo-1.13.0-release.apk` | 「不再复习这道题」跨设备同步（DB v18）+ 手机竖屏日历可收起 |
| 1.12.0 | 45 | `releases/BuErGuo-1.12.0-release.apk` | 批改分级输出 + 按需生成详解 + 题干图补发 |
| 1.11.0 | 44 | `releases/BuErGuo-1.11.0-release.apk` | 悬浮窗浏览器内核换成 GeckoView（修 DeepSeek 白屏） |
| 1.10.4 | 37 | `releases/BuErGuo-1.10.4-release.apk` | 光标守护补齐首字符与富文本聊天框 |
| 1.10.3 | 36 | `releases/BuErGuo-1.10.3-release.apk` | 修“输入一个字光标跳回开头” |
| 1.10.2 | 31 | `releases/BuErGuo-1.10.2-release.apk` | 窗口尺寸钉死 + ⓘ 计数 |
| 1.10.1 | 30 | `releases/BuErGuo-1.10.1-release.apk` | 悬浮窗三处真机反馈修复 |
| 1.10.0 | 29 | `releases/BuErGuo-1.10.0-release.apk` | 悬浮窗浏览器 AI + 公式渲染补齐 + 日历跳过跨设备 |
| 1.9.0 | 28 | `releases/BuErGuo-1.9.0-release.apk` | 考试记录自带题目快照（DB v17） |
| 1.8.5 | 27 | `releases/BuErGuo-1.8.5-release.apk` | AI 整套配置（含密钥）同步 |
| 1.8.4 | 26 | `releases/BuErGuo-1.8.4-release.apk` | 设置同步两处缺陷修复 |
| 1.8.3 | 25 | `releases/BuErGuo-1.8.3-release.apk` | AI 密钥可选同步 + 无用副本清理 |
| 1.8.2 | 24 | `releases/BuErGuo-1.8.2-release.apk` | 局域网文案 / 设置随同步 / 中文图片名 |
| 1.8.1 | 23 | `releases/BuErGuo-1.8.1-release.apk` | 局域网中文图片名 404 + MIUI 安装卡片 |
| 1.8.0 | 22 | `releases/BuErGuo-1.8.0-release.apk` | 数据板块重做、思考强度、全局搜索 |
| 1.7.1 | 21 | `releases/BuErGuo-1.7.1-release.apk` | |
| 1.7.0 | 20 | `releases/BuErGuo-1.7.0-release.apk` | 局域网面对面复制 |
| 1.6.1 | 19 | `releases/BuErGuo-1.6.1-release.apk` | 试卷批改分数显示 + 行内公式容错 |
| 1.6.0 | 18 | `releases/BuErGuo-1.6.0-release.apk` | 批改任务后台化（DB v14） |
| 1.5.0 | 17 | `releases/BuErGuo-1.5.0-release.apk` | 阶梯复习引擎（DB v13） |
| 1.4.2 | 16 | `releases/BuErGuo-1.4.2-release.apk` | |
| 1.4.1 | 15 | — | 该版本未在本仓库保留 APK 文件 |
| 1.4.0 | 14 | `releases/BuErGuo-1.4.0-release.apk` | DB v12 |
| 1.3.1 | 13 | `releases/BuErGuo-1.3.1-release.apk` | 复习排期天级化 |
| 1.3.0 | 12 | `releases/BuErGuo-1.3.0-release.apk` | DB v11 |
| 1.2.8 | 11 | `releases/BuErGuo-1.2.8-release.apk` | |
| 1.2.7 | 10 | `releases/BuErGuo-1.2.7-release.apk` | 识别成本优化等四项 |
| 1.2.3 | 6 | `releases/BuErGuo-1.2.3-release.apk` | |
| 1.2.2 | 5 | `releases/BuErGuo-1.2.2-release.apk` | |
| 1.2.1 | 4 | `releases/BuErGuo-1.2.1-release.apk` | |
| 1.2.0 | 3 | `releases/BuErGuo-1.2.0-release.apk` | |
