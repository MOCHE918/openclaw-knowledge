# MEMORY.md — 长期记忆

> 最后更新：2026-07-13

---

## 📜 铁律：记录一切

**每次下载 / 安装 / 登录 / 发布相关的操作，必须实时写入记忆文件**
路径：`D:\opencaw记忆录\YYYY-MM-DD.md`

禁止依赖对话缓存。对话被压缩后，记忆文件是唯一的线索。
这条铁律源自 2026-07-13 用户的明确要求。

---

## 👤 用户信息

- **称呼：** 直呼即可，不绕弯，不灌水
- **职业/兴趣：** 懂工程、会 Python、研究彩票数据分析、女儿11岁上小学
- **技术栈：** Windows 环境，便携版 OpenClaw，擅长 Pandas/Python 数据分析
- **时区：** Asia/Shanghai

---

## 🖥️ 系统环境（2026-07-13 快照）

### 磁盘
| 盘符 | 类型 | 总容量 | 剩余 | 用途 |
|------|------|--------|------|------|
| C: | 系统 SSD | 100 GB | ~48 GB | 系统盘 |
| D: | USB 3.0 U 盘 | 14.62 GB | ~3 GB ⚠️ | 便携盘 + OpenClaw |
| Z: | 虚拟盘 | ~14.9 TB | ~784 GB | 游戏/软件/数据盘 |

### 便携盘 D: 路径关键位置
- OpenClaw 工作区：`D:\Portable_V1.2.2\data\UserProfile\.openclaw\workspace\`
- Python：`D:\Portable_V1.2.2\data\UserProfile\AppData\local\Programs\Python\Python310\`
- pip 缓存：`D:\Portable_V1.2.2\data\UserProfile\AppData\local\pip\cache\`（~3 GB）
- 记忆文件：`D:\opencaw记忆录\`
- 技能目录：`~/.openclaw/workspace/skills/` （即 `D:\Portable_V1.2.2\data\UserProfile\.openclaw\workspace\skills\`）
- SSH 密钥：`~/.ssh/openclaw_agent_key`（D 盘 exFAT 不支持权限，需拷贝到 C: 用 icacls）

### 可用命令
- Python：WindowsApps 版（初始无 pip，需用户安装）
- Node.js：自带可用
- git：OpenClaw 自带
- 浏览器：Playwright Chromium
- 文档转换：Pandoc/LibreOffice 未安装

### 已发布的服务
- VPS：47.82.86.213，端口 22

---

## 📦 技能安装记录

| 日期 | 技能 | 来源 | 说明 |
|------|------|------|------|
| ~06-20 | skillhub-kit | 本地 | `D:\skillhub-kit\cli\` 管理技能安装 |
| 07-10 | zhouyi-advisor | clawhub | 《周易》智慧顾问 |
| 07-10 | fortuneteller | clawhub | 算命大师 |
| 07-10 | zhouyi-divin | clawhub | 周易占卜 |

---

## 🔄 常用工作流

### 彩票数据分析
- 双色球历史数据：`D:\双色球历史数据\`
- 使用：Pandas + Python 本地分析
- 生产报告：txt 预测文件

### SSH 连接 VPS
```
copy D:\...\.ssh\openclaw_agent_key C:\Users\Administrator\.ssh\
icacls C:\Users\Administrator\.ssh\openclaw_agent_key /reset
icacls C:\Users\Administrator\.ssh\openclaw_agent_key /inheritance:r /grant "Users:(R,W)"
```

### GitHub (MOCHE918)
- 邮箱：867812396@qq.com, 用户名：MOCHE918
- Token在VPS ~/.config/gh/hosts.yml
- 用途：作品集积累，不做直接变现

---

## 🚧 进行中的工作

### AI 生图 — 2026-07-13
- 目标：搭建 Stable Diffusion 生图环境
- 状态（22:46）：**安装中断**
- 已装：numpy, PIL, sympy, networkx 等基础包（~145 MB）
- 中断：PyTorch (torch 2.3.1+cu121) 安装未完成
- 未装：diffusers, transformers, accelerate, xformers
- 问题：D 盘只剩 3 GB，不够装模型
- 方向：建议用 Z 盘（784 GB 空闲）或清理 pip 缓存
- 来源：待用户确认（从哪下载的 SD）

### 搬运生图到作品文件夹
- 生图后要搬到 C 盘（待用户指定具体路径）
- 作品文件夹尚未创建

---

## ⚠️ 已知风险 / 注意事项

1. **D 盘空间极有限** — 14.62 GB 总容量，剩 3 GB，大文件操作先确认剩余
2. **对话压缩丢失记忆** — 务必写文件，MEMORY.md 有被清空历史的记录
3. **exFAT 权限限制** — D 盘若是 exFAT，SSH 密钥等需拷到 C 盘
4. **Python 环境在便携盘** — pip 安装的包会吃 D 盘空间
5. **🔴 app.zip 不可删除！** — `H:\Portable_V1.2.2\app.zip` 是便携版启动核心文件。2026-07-14 事故：误删导致外电脑无法启动。严禁列入清理清单！
6. **H 盘是便携安装盘** — 插到外电脑时 `H:\Portable_V1.2.2\` 是启动根目录，所有文件必须完整
