# 下载与文件校验

## 官方下载来源

轻变计划 v3.8.2 提供以下官方来源：

1. 官网 APK：
   <https://img.qbplan.cn/apk/qbplan-v3.8.2-release.apk>
2. GitHub Release：
   <https://github.com/PingRan/qbplan-android/releases/tag/v3.8.2>

不要从来源不明、版本信息不完整或无法核对来源的第三方页面下载安装包。

从官网或本仓库的正式Release直接下载时，普通用户不需要在每次安装前重复计算哈希。SHA-256主要用于：

- 核对官网与GitHub提供的是否为同一个文件；
- 检查经过缓存、镜像或转存后的文件是否发生变化；
- 排查下载损坏或来源不明的问题；
- 对外记录每个正式版本对应的唯一安装文件。

## 文件信息

| 项目 | 内容 |
|---|---|
| 文件名 | `qbplan-v3.8.2-release.apk` |
| 文件大小 | 12,315,345 字节 |
| 包名 | `com.qbplan.app` |
| 版本 | v3.8.2 |
| versionCode | 40 |

SHA-256：

```text
F187F8AA9FFB6A131AD2B26BD6EC14C7D1E26F7F7A10BBC7AEA875ED0039E60B
```

## Windows 校验方法

在 PowerShell 中运行：

```powershell
Get-FileHash -LiteralPath ".\qbplan-v3.8.2-release.apk" -Algorithm SHA256
```

输出的 `Hash` 必须与本页公布的 SHA-256 完全一致。

## macOS 校验方法

在终端运行：

```bash
shasum -a 256 qbplan-v3.8.2-release.apk
```

## Linux 校验方法

在终端运行：

```bash
sha256sum qbplan-v3.8.2-release.apk
```

## 校验不一致怎么办

如果哈希不一致：

1. 不要安装该文件；
2. 删除已下载的文件；
3. 从官网或本仓库的正式 Release 重新下载；
4. 如问题持续存在，请联系 <qbplan@163.com>。
