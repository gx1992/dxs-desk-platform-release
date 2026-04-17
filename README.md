# dxs-desk-platform Release

Agile Tauri 桌面应用发布仓库（GitHub 备份）

---

## 最新版本: v0.2.4

| 平台 | 下载链接 |
|------|---------|
| Windows x64 | [DXS-AI._0.2.4_x64-setup.exe](releases/v0.2.4/DXS-AI._0.2.4_x64-setup.exe) |
| macOS Apple Silicon | [DXS-AI._0.2.4_aarch64.dmg](releases/v0.2.4/DXS-AI._0.2.4_aarch64.dmg) |
| macOS Intel | [DXS-AI._0.2.4_x64.dmg](releases/v0.2.4/DXS-AI._0.2.4_x64.dmg) |

---

## 版本历史

### v0.2.4 (2026-04-17)

- 新增 WebView 隐藏窗口抓取 SPA 网站内容，最大并发 3 个
- AI 分析支持招投标专项分析，提取公告列表及日期
- 优化 AI 快速分析速度（精简 prompt、限制 token）
- 自动更新检查间隔调整为 2 分钟
- 优化局域网通信功能

### v0.2.3 (2026-04-17)

- 新增网址订阅监控功能（可配置多个 URL，定时抓取，内容哈希去重）
- 支持后台调度器自动检测更新，推送前端事件刷新
- 支持 AI 摘要分析与快照差量对比
- 修复：调度器改用 tauri::async_runtime::spawn，解决启动 panic

### v0.2.1 (2026-04-17)

- 新增应用内更新提示功能（标题栏绿色胶囊按钮，2 小时自动检测）
- 重设计 UK 品牌图标（与 Web 系统一致）
- 窗口标题改为 DXS-AI文档助手

### v0.2.0 (2026-04-17)

- 新增 AI 助手、项目管理、报价单等核心功能
- 新增应用内自动更新功能

### v0.1.0 (2026-04-16)

- 首次发布
- 支持 Windows x64 / macOS Apple Silicon / macOS Intel

---

## 目录结构

```
releases/
├── v0.2.4/
│   ├── DXS-AI._0.2.4_x64-setup.exe               # Windows 安装包
│   ├── DXS-AI._0.2.4_x64-setup.exe.sig           # Windows 签名
│   ├── DXS-AI._0.2.4_x64-setup.nsis.zip          # Windows 自动更新包
│   ├── DXS-AI._0.2.4_x64-setup.nsis.zip.sig      # Windows 自动更新签名
│   ├── DXS-AI._0.2.4_aarch64.dmg                 # macOS Apple Silicon 安装包
│   ├── DXS-AI._aarch64.app.tar.gz                # macOS ARM 自动更新包
│   ├── DXS-AI._aarch64.app.tar.gz.sig            # macOS ARM 自动更新签名
│   ├── DXS-AI._0.2.4_x64.dmg                    # macOS Intel 安装包
│   ├── DXS-AI._x64.app.tar.gz                   # macOS Intel 自动更新包
│   └── DXS-AI._x64.app.tar.gz.sig               # macOS Intel 自动更新签名
├── v0.2.3/
│   ├── dxs-desk_0.2.3_x64-setup.exe           # Windows 安装包
│   ├── dxs-desk_0.2.3_x64-setup.exe.sig       # Windows 签名
│   ├── dxs-desk_0.2.3_x64-setup.nsis.zip      # Windows 自动更新包
│   ├── dxs-desk_0.2.3_x64-setup.nsis.zip.sig  # Windows 自动更新签名
│   ├── dxs-desk_0.2.3_aarch64.dmg             # macOS Apple Silicon 安装包
│   ├── dxs-desk_aarch64.app.tar.gz            # macOS ARM 自动更新包
│   ├── dxs-desk_aarch64.app.tar.gz.sig        # macOS ARM 自动更新签名
│   ├── dxs-desk_0.2.3_x64.dmg                # macOS Intel 安装包
│   ├── dxs-desk_x64.app.tar.gz               # macOS Intel 自动更新包
│   └── dxs-desk_x64.app.tar.gz.sig           # macOS Intel 自动更新签名
├── v0.2.1/
│   ├── dxs-desk_0.2.1_x64-setup.exe           # Windows 安装包
│   ├── dxs-desk_0.2.1_x64-setup.exe.sig       # Windows 签名
│   ├── dxs-desk_0.2.1_x64-setup.nsis.zip      # Windows 自动更新包
│   ├── dxs-desk_0.2.1_x64-setup.nsis.zip.sig  # Windows 自动更新签名
│   ├── dxs-desk_0.2.1_aarch64.dmg             # macOS Apple Silicon 安装包
│   ├── dxs-desk_aarch64.app.tar.gz            # macOS ARM 自动更新包
│   ├── dxs-desk_aarch64.app.tar.gz.sig        # macOS ARM 自动更新签名
│   ├── dxs-desk_0.2.1_x64.dmg                # macOS Intel 安装包
│   ├── dxs-desk_x64.app.tar.gz               # macOS Intel 自动更新包
│   └── dxs-desk_x64.app.tar.gz.sig           # macOS Intel 自动更新签名
├── v0.2.0/
│   ├── dxs-desk_0.2.0_x64-setup.exe           # Windows 安装包
│   ├── dxs-desk_0.2.0_x64-setup.exe.sig       # Windows 签名
│   ├── dxs-desk_0.2.0_x64-setup.nsis.zip      # Windows 自动更新包
│   ├── dxs-desk_0.2.0_x64-setup.nsis.zip.sig  # Windows 自动更新签名
│   ├── dxs-desk_0.2.0_aarch64.dmg             # macOS Apple Silicon 安装包
│   ├── dxs-desk_aarch64.app.tar.gz            # macOS ARM 自动更新包
│   ├── dxs-desk_aarch64.app.tar.gz.sig        # macOS ARM 自动更新签名
│   ├── dxs-desk_0.2.0_x64.dmg                # macOS Intel 安装包
│   ├── dxs-desk_x64.app.tar.gz               # macOS Intel 自动更新包
│   └── dxs-desk_x64.app.tar.gz.sig           # macOS Intel 自动更新签名
└── v0.1.0/
    ├── Agile.Tauri_0.1.0_x64-setup.exe           # Windows 安装包
    ├── Agile.Tauri_0.1.0_x64-setup.exe.sig       # Windows 签名
    ├── Agile.Tauri_0.1.0_x64-setup.nsis.zip      # Windows 自动更新包
    ├── Agile.Tauri_0.1.0_x64-setup.nsis.zip.sig  # Windows 自动更新签名
    ├── Agile.Tauri_0.1.0_aarch64.dmg             # macOS Apple Silicon 安装包
    ├── Agile.Tauri_aarch64.app.tar.gz             # macOS ARM 自动更新包
    ├── Agile.Tauri_aarch64.app.tar.gz.sig         # macOS ARM 自动更新签名
    ├── Agile.Tauri_0.1.0_x64.dmg                 # macOS Intel 安装包
    ├── Agile.Tauri_x64.app.tar.gz                # macOS Intel 自动更新包
    └── Agile.Tauri_x64.app.tar.gz.sig            # macOS Intel 自动更新签名
update.json                                        # 自动更新端点
```
