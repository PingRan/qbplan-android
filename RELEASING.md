# 轻变计划 Android 发布流程

本流程适用于 v3.8.2、v3.9.0 等后续正式版本。

## 1. 确认正式版本

发布前确认：

- `versionName` 与计划发布版本一致；
- `versionCode` 大于上一正式版本；
- 包名仍为 `com.qbplan.app`；
- 使用正式签名构建；
- APK来自最终正式构建，不使用测试包或临时包；
- 已完成必要的真机功能检查。

建议文件名保持统一：

```text
qbplan-v3.8.2-release.apk
```

不要覆盖或复用旧版本文件名。

## 2. 检查权限、隐私和产品事实变化

比较新版本与上一版本：

- 是否新增、删除或改变 Android 权限；
- 无障碍服务、应用使用情况访问或悬浮窗用途是否变化；
- 是否新增数据字段、上传条件、第三方 SDK 或保存期限；
- Android 支持范围是否变化；
- 核心守护流程是否变化；
- 支持的应用或厂商范围是否变化；
- 开发者主体、用户协议或隐私政策是否变化。

如果权限或数据处理发生变化，必须先更新隐私政策和应用市场资料，再发布安装包和对外说明。

## 3. 计算安装包信息

记录：

- 文件名；
- 文件大小；
- SHA-256；
- versionName；
- versionCode；
- 发布日期；
- 包名；
- 正式签名信息。

Windows PowerShell校验：

```powershell
Get-FileHash -LiteralPath ".\qbplan-v3.8.2-release.apk" -Algorithm SHA256
```

## 4. 更新仓库文档

每次正式发布至少更新：

### `README.md`

- 当前版本；
- versionCode；
- 发布日期；
- 文件名；
- 文件大小；
- SHA-256；
- GitHub Release链接；
- Android支持范围（如有变化）。

### `CHANGELOG.md`

在旧版本上方新增版本章节，不删除历史版本：

```markdown
## v3.8.2

- 版本号：`3.8.2`
- versionCode：`新的值`
- 发布日期：`YYYY-MM-DD`

### 主要变化

- ...

### 修复

- ...
```

只写真实、可以公开核验的变化。

### `SHA256SUMS.txt`

保留旧版本记录，并在顶部或底部增加新版本：

```text
新的SHA-256  qbplan-v3.8.2-release.apk
```

### `release-notes/v3.8.2.md`

为新版本建立独立Release说明，包含：

- 产品一句话定义；
- 版本信息；
- 主要变化；
- 已知限制；
- APK文件名、大小和SHA-256；
- 官网及隐私政策链接；
- 非开源仓库说明。

### 其他文档

仅在事实发生变化时更新：

- `docs/how-it-works.md`
- `docs/download-and-verify.md`
- `docs/known-limitations.md`
- `SECURITY.md`
- `NOTICE.md`

## 5. 更新官网

在创建GitHub Release前或同时更新：

- 官网正式APK；
- `/download.html`；
- `/what-is-qbplan.html`中的当前版本、日期、大小和哈希；
- 下载接口返回的版本信息；
- 页面中的结构化数据；
- sitemap的`lastmod`（仅对实际修改的页面更新）。

旧版本URL如继续提供下载，应明确标注为历史版本。

## 6. 提交文档

先提交文档和版本记录，再创建Release。

建议提交信息：

```text
publish qbplan android v3.8.2
```

确认Git仓库中没有APK、AAB、JKS、keystore、密码或其他敏感文件。

## 7. 创建GitHub Release

创建：

```text
Tag：v3.8.2
Release标题：轻变计划 v3.8.2
```

Release正文使用：

```text
release-notes/v3.8.2.md
```

上传两个Release资源：

```text
qbplan-v3.8.2-release.apk
SHA256SUMS-v3.8.2.txt
```

Release资源只上传最终正式文件，不上传测试包。

## 8. 发布后校验

发布完成后检查：

1. GitHub Release页面可以公开访问；
2. APK能够正常下载；
3. 下载后的文件大小与本地一致；
4. 下载后的SHA-256与发布记录一致；
5. 官网和GitHub下载的是同一个正式APK；
6. README、官网、Release和应用市场版本信息一致；
7. 旧版本Release仍然保留；
8. 没有把源码私有仓库、签名文件或密钥公开。

## 9. 应用市场和外部内容

同步更新：

- 应用市场版本与更新说明；
- B站、知乎等官方账号中的当前版本信息（仅在相关内容涉及具体版本时）；
- 对外功能演示说明；
- 已知兼容问题。

不要删除或改写旧版本内容使其看起来像新版本；需要时添加“该内容演示的是v3.8.1”等历史版本标识。

## 10. 版本发布原则

- 一个正式版本对应一个唯一Tag；
- 一个Tag对应一个不可混淆的Release；
- 不覆盖旧APK；
- 不复用旧哈希；
- 不把公开仓库描述为开源仓库；
- 不在未同步隐私和应用市场资料时发布涉及新增权限或数据处理的新版本；
- 不为了GEO制造不存在的功能、效果或用户反馈。
