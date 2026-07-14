# TOOLS.md — 本地工具清单

Skills 定义工具怎么用。这个文件记录你的具体环境配置。

---

## 系统可调用工具

| 工具 | 状态 | 来源 |
|------|------|------|
| python | ✅ | WindowsApps（Microsoft Store Python） |
| git | ✅ v2.53.0 | OpenClaw 自带（git\cmd） |
| curl | ✅ | Windows 系统 |
| wget | ✅ | Windows 系统 |
| bash/grep/sed/awk | ✅ | OpenClaw 自带（git\mingw64, git\usr） |
| SSH 密钥 | ✅ | `~/.ssh/openclaw_agent_key` |

## OpenClaw 内置 npm 能力（workspace 内可直接使用）

- **pdf-parse / pdfjs-dist** — PDF 解析、提取文字/表格
- **xlsx** — Excel 文件读写（.xlsx/.xls/.csv）
- **html-to-docx** — HTML→Word 文档生成
- **@napi-rs/canvas** — Skia 画布（创建/编辑图片）
- **htmlparser2 / xmlbuilder2** — HTML/XML 解析与构建
- **@noble/ciphers / @noble/hashes** — 加解密算法
- **node-fetch** — HTTP 请求
- **brotli** — 压缩/解压缩

## 已安装技能 & 插件

- **Playwright** — Chromium headless (v148)，用于动态页面抓取
  - 安装位置：`C:\Users\Administrator\node_modules\playwright`
  - 用途：彩票数据官方 API 抓取、百度文库等动态页面
- **AnySearch 搜索技能** — `anysearch-skill` 部署，API Key 已配
- **MiniMax 图像理解** — `minimax-understand-image` 技能
- **周易智慧顾问** — `zhouyi-advisor` (clawhub, 2026-07-10安装)
- **算命大师** — `fortuneteller` (clawhub, 2026-07-10安装)
- **周易占卜** — `zhouyi-divin` (clawhub, 2026-07-10安装)
- **Skillhub CLI** — `D:\skillhub-kit\cli\`，管理技能安装

## API Keys

- `ACE_MUSIC_API_KEY`: 183598988a4241109b21b78475fc4d5e
- `ANYSEARCH_API_KEY`: as_sk_02d27c9dc605bfdac9a707784c047c67

## 输出目录

- 音乐/歌曲 → `D:\墨澈的音乐\`
- 教材/课件PPT → `D:\墨澈的教材\`

## SSH 密钥

- 密钥文件在 `D:\...\.ssh\`，但 D 盘（便携盘）可能是 exFAT/FAT32，**不支持文件权限**
- OpenSSH 要求私钥文件权限严格，便携盘上无法设置
- **解决方案：**使用时先复制到 `C:\Users\Administrator\.ssh\`，用 icacls 设置权限
  ```
  copy D:\...\.ssh\openclaw_agent_key C:\Users\Administrator\.ssh\
  icacls C:\Users\Administrator\.ssh\openclaw_agent_key /reset
  icacls C:\Users\Administrator\.ssh\openclaw_agent_key /inheritance:r /grant "Users:(R,W)"
  ```
- VPS: 47.82.86.213 (admin@), 端口 22

## 新装 Node 包

- `playwright-extra` v4.3.6 — Playwright 插件系统
- `puppeteer-extra-plugin-stealth` v2.11.2 — stealth 模式
- 安装方式：`cmd /c npm install <pkg>`（PS 禁止执行 npm.ps1）

## 系统限制

- **.bat 文件双击无效** — 无法通过双击执行批处理脚本
- 需要运行脚本时，走 PowerShell 或 OpenClaw 内 exec
- **无 root/管理员工具：** choco、winget、VSCode 均未安装
- **无多媒体处理：** ffmpeg 未安装（无法转换音视频格式）
- **无文档转换引擎：** Pandoc、LibreOffice 均未安装
