# dxs-desk-platform Release

Agile Tauri 桌面应用发布仓库（GitHub 备份）

---

## 最新版本: v0.2.0

| 平台 | 下载链接 |
|------|---------|
| Windows x64 | [dxs-desk_0.2.0_x64-setup.exe](releases/v0.2.0/dxs-desk_0.2.0_x64-setup.exe) |
| macOS Apple Silicon | [dxs-desk_0.2.0_aarch64.dmg](releases/v0.2.0/dxs-desk_0.2.0_aarch64.dmg) |
| macOS Intel | [dxs-desk_0.2.0_x64.dmg](releases/v0.2.0/dxs-desk_0.2.0_x64.dmg) |

---

## 版本历史

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
