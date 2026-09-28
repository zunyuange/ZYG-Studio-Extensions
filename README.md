# ZYG-Studio 扩展发布包（zyg-extensions-release）

ZYG-Studio 扩展中心的正式发布清单，命名规范 **`ZYG-Studio-*.mcext`**（单横线）。

## 内容

| 文件 | 说明 |
| --- | --- |
| `release-manifest.json` | 15 个扩展包的 name / bytes / sha256 / download_url |
| `SHA256SUMS` | 标准校验和文件（`sha256sum -c SHA256SUMS` 可验证） |

- 扩展包本体位于：`apk\MobiCode-Extensions-main\ZYG-Studio-Extensions\`（15 个 `ZYG-Studio-*.mcext`，共约 2.1 GB）
- 生成脚本：`docs\scripts\generate_zyg_manifest.py`（对本地文件实测 sha256 与字节数，并与官方 SHA256SUMS 交叉核对——**15/15 全部一致**）

## 上传到 GitHub Release（v2026.09.28 tag）✅ 已发布

下载根（代码中 `RELEASE_BASE` 已指向，**资产已上传并验证匿名可下载**）：

```
https://github.com/zunyuange/ZYG-Studio-Extensions/releases/download/v2026.09.28
```

发布状态（2026-09-28 实测）：

- 15 个 `ZYG-Studio-*.mcext` 已上传至公开仓库 `zunyuange/ZYG-Studio-Extensions` 的 Release `v2026.09.28`
- 抽查 git / python / apktool / rust / lua 下载链接均返回 200，字节数与 manifest 精确一致
- Release 页面：https://github.com/zunyuange/ZYG-Studio-Extensions/releases/tag/v2026.09.28

## 下载 URL 模式

```text
https://github.com/zunyuange/ZYG-Studio-Extensions/releases/download/v2026.09.28/ZYG-Studio-<工具>-v<版本>.mcext
```

> 注意：Release 资产下载必须用 `/releases/download/<tag>/<file>`（tag 页 `/releases/tag/<tag>` 仅作浏览，不能拼文件名）。

## 校验方法

```bash
# Linux/macOS
cd <扩展包目录> && sha256sum -c docs/zyg-extensions-release/SHA256SUMS
```

## Package policy

- Only the current published extension set is included.
- Historical duplicates, temporary archives, server files, passwords, and private configuration are excluded.
- Verify every downloaded package against `SHA256SUMS` before installation.

## Current packages

| Package | Purpose |
| --- | --- |
| `ZYG-Studio-Lua-Android-v1.4.0.mcext` | Lua Android runtime |
| `ZYG-Studio-Codex-Runtime-v2.1.0.mcext` | AI runtime |
| `ZYG-Studio-Java-Android-v2.1.2.mcext` | Android Java build environment |
| `ZYG-Studio-ripgrep-v14.1.1.mcext` | `rg` search tool |
| `ZYG-Studio-git-v2.55.0.mcext` | Git version control |
| `ZYG-Studio-openssh-v10.5p1.mcext` | SSH/SFTP tools |
| `ZYG-Studio-python-v3.14.6.mcext` | Python runtime |
| `ZYG-Studio-nodejs-v26.4.0.1.mcext` | Node.js and npm |
| `ZYG-Studio-php-web-v8.5.1.1.mcext` | PHP web runtime |
| `ZYG-Studio-sqlite-v3.53.4.mcext` | SQLite CLI |
| `ZYG-Studio-apktool-v3.0.3.mcext` | APK and Smali tools |
| `ZYG-Studio-openjdk-v21.0.12.mcext` | OpenJDK |
| `ZYG-Studio-golang-v1.26.5.mcext` | Go runtime |
| `ZYG-Studio-rust-v1.97.1.1.mcext` | Rust runtime |
| `ZYG-Studio-clang-v21.1.8.1.mcext` | Clang/LLVM C/C++ toolchain |


---
© 尊缘阁（ZYG）· ZYG-Studio
