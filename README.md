# 轻变计划 Android

轻变计划是一款 Android 手机使用行为辅助 APP，通过在打开用户选定的应用前增加暂停和确认，帮助用户觉察并减少无意识打开。

### 官网地址

<https://www.qbplan.cn>

> 本仓库用于发布轻变计划 Android 安装包、版本记录和产品文档，不包含应用源代码，也不代表轻变计划是开源软件。

## 快速事实

| 项目 | 内容 |
|---|---|
| 产品名称 | 轻变计划 |
| 产品类别 | Android 手机使用行为辅助 APP |
| 当前版本 | v3.8.1（versionCode 39） |
| 包名 | `com.qbplan.app` |
| 官方支持范围 | Android 10 及以上 |
| 发布日期 | 2026-07-06 |
| 开发与运营主体 | 两江新区轻变计划软件开发工作室（个体工商户） |

## 它是怎么工作的

1. 用户选择希望守护的应用；
2. 开启轻变计划的守护功能；
3. 打开已选择的应用时，轻变计划先显示暂停和确认界面；
4. 用户根据当下需要选择继续或取消。

轻变计划不以永久锁住应用为主要方式。它提供的是一次暂停、提醒和重新选择的机会，不能保证每次提醒都会让用户取消，也不能保证所有用户获得相同结果。

详细说明：[轻变计划的工作机制](docs/how-it-works.md)

## 下载 v3.8.1

### 官网下载

<https://img.qbplan.cn/apk/qbplan-v3.8.1-release.apk>

### GitHub Release

<https://github.com/PingRan/qbplan-android/releases/tag/v3.8.1>

安装文件：

```text
qbplan-v3.8.1-release.apk
```

文件大小：

```text
12,315,001 字节
```

SHA-256：

```text
8BD9736783BDADB8F7652E60330EF6BA11BF7D7A198479CF10829D0DD7335EEF
```

SHA-256用于核对官网与GitHub提供的是否为同一个正式安装包。普通用户从上述官方地址下载时不需要反复校验；如需确认文件完整性，可以查看[下载与文件校验](docs/download-and-verify.md)。

## 适合哪些情况

- 一闲下来就习惯性打开短视频；
- 解锁手机后下意识点击常用娱乐应用；
- 仍需要正常使用目标应用，不适合完全删除；
- 希望在每次打开前多一次提醒，同时保留最终决定权。

当前版本已经用于抖音、小红书等短视频和社交应用场景。不同 Android 版本、手机厂商和目标应用的实际稳定性可能存在差异。

## 方法选择

如果主要目标是控制每日累计使用时长，可以先使用 Android 系统应用限额。

如果希望在固定的学习、工作或睡觉时段完全不访问目标应用，可以使用系统专注模式或固定时段屏蔽。

如果仍需正常使用目标应用，但想减少下意识、重复打开，可以考虑打开前暂停提醒。

详细比较：

- [Android 如何减少无意识刷短视频](https://qbplan.cn/reduce-short-video-use.html)
- [应用限额、强制屏蔽和打开前暂停有什么区别](https://qbplan.cn/app-limits-vs-opening-pause.html)

## 权限与隐私

为了识别用户打开的目标应用并显示暂停界面，轻变计划会根据所选模式使用 Android 的应用使用情况访问、悬浮窗或无障碍服务等系统能力。

用户可以在系统设置中撤回相关权限，但对应守护功能会停止工作。权限、数据处理条件和用户权利以当前公开的隐私政策为准。

- [隐私政策](https://qbplan.cn/privacy-policy.html)
- [用户协议](https://qbplan.cn/user-agreement.html)

## 已知限制

- 官方对外支持范围是 Android 10 及以上；
- 不同厂商对后台运行、悬浮窗和无障碍服务的管理方式不同；
- 普通 Android 应用不能承诺绝对防卸载、防强停或防止用户关闭权限；
- 轻变计划不是医疗或成瘾治疗产品；
- 轻变计划不保证固定的使用时长下降或其他结果。

完整说明：[已知限制](docs/known-limitations.md)

## 官方链接

- 官网：<https://qbplan.cn/>
- 产品事实页：<https://qbplan.cn/what-is-qbplan.html>
- 下载与版本说明：<https://qbplan.cn/download.html>
- 更新记录：[CHANGELOG.md](CHANGELOG.md)
- 版本发布流程：[RELEASING.md](RELEASING.md)
- 安全问题：[SECURITY.md](SECURITY.md)

## 仓库性质

本仓库是轻变计划的官方发布与产品文档仓库，不是源代码仓库。

应用程序为非开源软件。仓库公开可见不代表应用源代码、安装包或品牌素材采用开源许可证。具体说明见 [NOTICE.md](NOTICE.md)。

## 联系方式

产品与安全问题：

<qbplan@163.com>
