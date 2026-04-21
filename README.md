# dxs-desk-platform Release

Agile Tauri 桌面应用发布仓库（GitHub 备份）

---

## 最新版本: v0.2.7

| 平台 | 下载链接 |
|------|---------|
| Windows x64 | [DXS-AI._0.2.7_x64-setup.exe](releases/v0.2.7/DXS-AI._0.2.7_x64-setup.exe) |
| macOS Apple Silicon | [DXS-AI._0.2.7_aarch64.dmg](releases/v0.2.7/DXS-AI._0.2.7_aarch64.dmg) |
| macOS Intel | [DXS-AI._0.2.7_x64.dmg](releases/v0.2.7/DXS-AI._0.2.7_x64.dmg) |

---

## 版本历史

### v0.2.7 (2026-04-21)

- 监控公告支持点击跳转详情链接（从 [LINKS] 区块精确匹配）
- 修复点击公告时应用崩溃问题（UTF-8 多字节字符安全切片）
- AI 摘要报告公告项美化为绿色卡片样式（与差量对比报告一致）
- WebView 抓取时附加 [LINKS] 区块，记录页面所有 <a href> 链接
- AI prompt 优化为 `标题 | 日期 | URL` 格式，自动从链接表填充 URL

### v0.2.6 (2026-04-21)

- RAG 向量检索与 AI 对话打通，知识库语义搜索结果融入回答上下文
- 修复 MCP 工具名含中文或点号导致 AI 接口 400 错误
- 知识库导入文件后自动后台建索引，底部显示索引状态
- 知识库新增"向这个知识库提问"AI 快捷入口
- 知识库空白状态改为三步引导卡片
- 嵌入模型配置新增测试连接按钮
- 修复知识库文件"打开所在目录"路径丢失问题

### v0.2.5 (2026-04-20)

- 新增局域网群组通信（群创建、成员管理、群消息收发）
- 支持聊天附件（文件/图片）一键保存到项目并触发 AI 索引
- 修复数据库版本迁移崩溃问题（v8→v19）
- 空间文件树改用虚拟滚动，文件数量多时不再卡顿
- 文件树默认折叠，仅展开根层；图标与文件名同行显示

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
├── v0.2.7/
│   ├── DXS-AI._0.2.7_x64-setup.exe               # Windows 安装包
│   ├── DXS-AI._0.2.7_x64-setup.exe.sig           # Windows 签名
│   ├── DXS-AI._0.2.7_x64-setup.nsis.zip          # Windows 自动更新包
│   ├── DXS-AI._0.2.7_x64-setup.nsis.zip.sig      # Windows 自动更新签名
│   ├── DXS-AI._0.2.7_aarch64.dmg                 # macOS Apple Silicon 安装包
│   ├── DXS-AI._aarch64.app.tar.gz                # macOS ARM 自动更新包
│   ├── DXS-AI._aarch64.app.tar.gz.sig            # macOS ARM 自动更新签名
│   ├── DXS-AI._0.2.7_x64.dmg                    # macOS Intel 安装包
│   ├── DXS-AI._x64.app.tar.gz                   # macOS Intel 自动更新包
│   └── DXS-AI._x64.app.tar.gz.sig               # macOS Intel 自动更新签名
├── v0.2.6/
│   ├── DXS-AI._0.2.6_x64-setup.exe               # Windows 安装包
│   ├── DXS-AI._0.2.6_x64-setup.exe.sig           # Windows 签名
│   ├── DXS-AI._0.2.6_x64-setup.nsis.zip          # Windows 自动更新包
│   ├── DXS-AI._0.2.6_x64-setup.nsis.zip.sig      # Windows 自动更新签名
│   ├── DXS-AI._0.2.6_aarch64.dmg                 # macOS Apple Silicon 安装包
│   ├── DXS-AI._aarch64.app.tar.gz                # macOS ARM 自动更新包
│   ├── DXS-AI._aarch64.app.tar.gz.sig            # macOS ARM 自动更新签名
│   ├── DXS-AI._0.2.6_x64.dmg                    # macOS Intel 安装包
│   ├── DXS-AI._x64.app.tar.gz                   # macOS Intel 自动更新包
│   └── DXS-AI._x64.app.tar.gz.sig               # macOS Intel 自动更新签名
├── v0.2.5/
│   ├── DXS-AI._0.2.5_x64-setup.exe               # Windows 安装包
│   ├── DXS-AI._0.2.5_x64-setup.exe.sig           # Windows 签名
│   ├── DXS-AI._0.2.5_x64-setup.nsis.zip          # Windows 自动更新包
│   ├── DXS-AI._0.2.5_x64-setup.nsis.zip.sig      # Windows 自动更新签名
│   ├── DXS-AI._0.2.5_aarch64.dmg                 # macOS Apple Silicon 安装包
│   ├── DXS-AI._aarch64.app.tar.gz                # macOS ARM 自动更新包
│   ├── DXS-AI._aarch64.app.tar.gz.sig            # macOS ARM 自动更新签名
│   ├── DXS-AI._0.2.5_x64.dmg                    # macOS Intel 安装包
│   ├── DXS-AI._x64.app.tar.gz                   # macOS Intel 自动更新包
│   └── DXS-AI._x64.app.tar.gz.sig               # macOS Intel 自动更新签名
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
