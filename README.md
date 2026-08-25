# Sylara
Sylara —— 为音乐收藏家打造的精致本地音乐播放器。支持逐字歌词（卡拉OK效果）与独立桌面歌词悬浮窗，沉浸式毛玻璃UI，智能听歌报告，高颜值且纯粹。
# 🎵 Sylara · Your Wave

> 一款为「本地音乐收藏家」量身打造的桌面音乐播放器。  
> 不联网、不采集、不社交 —— 只专注你拥有的每一首歌。

<img width="1053" height="766" alt="首页" src="https://github.com/user-attachments/assets/bd886bc6-07d3-4189-b62f-fec2276a61cc" />

---
<img width="1053" height="766" alt="多种排版模式" src="https://github.com/user-attachments/assets/ea3b0f13-0e30-46c2-b360-b6a19cee5f15" />
<img width="1053" height="766" alt="多种排序方式" src="https://github.com/user-attachments/assets/56b45fcf-2168-4a12-980d-9fae1009f52c" />
设置功能多样
<img width="1053" height="766" alt="设置功能多" src="https://github.com/user-attachments/assets/9bdba844-75f2-43a6-a961-07d95db414d7" />
<img width="1053" height="766" alt="多种设置" src="https://github.com/user-attachments/assets/584e99a1-d1f4-49be-b138-626091ff3a8e" />
<img width="1053" height="766" alt="可在线记录播放" src="https://github.com/user-attachments/assets/9b24b4a6-33fb-4e39-9217-1e13c016985e" />
可在线记录播放
## ✨ 核心亮点
<img width="1053" height="766" alt="可使用浅色 深色 歌曲封面作为背景三种模式" src="https://github.com/user-attachments/assets/e06c4e4d-7b4a-4d49-8e2a-fd53998cfdbf" />
<img width="453" height="83" alt="支持多种桌面歌词显示（详细见设置）" src="https://github.com/user-attachments/assets/b82a049d-7e43-44b8-8970-a82ea78fe24e" />
<img width="1053" height="766" alt="支持收藏导入导出" src="https://github.com/user-attachments/assets/1f376863-2d56-4626-a82c-6e5edddb777f" />
<img width="1053" height="766" alt="支持歌单 导入导出等" src="https://github.com/user-attachments/assets/a096a7d5-bd03-41ad-bd9b-34259b59951a" />
<img width="1053" height="766" alt="沉浸歌词模式" src="https://github.com/user-attachments/assets/a082b16f-57e8-4fe6-bafd-34ee04439573" />
<img width="1053" height="766" alt="多种听歌报告" src="https://github.com/user-attachments/assets/56273775-6b9b-48e0-803d-55c669abebd7" />

### 🎤 逐字歌词 & 桌面悬浮窗
- **全屏沉浸歌词页**：逐字高亮（卡拉OK效果），实时跟随播放进度滚动。
- **独立桌面歌词窗口**：**鼠标穿透锁定**（边玩游戏边看歌词）、拖拽移动、独立字号/主题调节。
- **智能空格算法**：中文不拆字，英文留间隙，标点不突兀。

### 🎨 动态视觉设计
- **封面智能取色**：提取专辑封面主色调，生成渐变背景，亮色封面自动切换深色文字。
- **毛玻璃 & 动态模糊**：沉浸式模糊背景，媲美 Apple Music 的质感。
- **浅色 / 深色主题**：跟随系统或手动切换，所有 UI 组件同步适配。

### 📂 音乐库管理
- **多维度浏览**：按歌曲、专辑、歌手、文件夹、自定义歌单灵活组织。
- **智能“今日推荐”**：根据收藏、播放次数与遗忘曲线生成专属推荐歌单。
- **批量导入**：单文件/文件夹/拖拽导入，自动解析标签与内嵌封面。

### ⚙️ 专业音频工具
- **5段均衡器**：Web Audio 实时处理，内置流行/摇滚/爵士等预设。
- **波形进度条**：可视化音频波形，大文件自动跳过防止卡顿。
- **三阶段重复检测**：大小 → 采样哈希 → 全量哈希，精准定位重复文件。

### 📊 数据洞察
- **本地听歌报告**：周/月/季/年维度，可视化播放趋势，**一键导出 PDF**。
- **ListenBrainz 集成**：可选云端同步收听记录（Scrobble），支持拉取云端历史合并到报告。

---

## 🛠 技术栈

| 层级 | 技术选型 |
| :--- | :--- |
| **框架** | Electron 43 + Node.js |
| **渲染引擎** | 原生 JavaScript（ES Module 模块化） |
| **音频解析** | music-metadata + node-id3 |
| **歌词引擎** | 自研解析器（支持 LRC / 逐字时间轴） |
| **数据持久化** | localStorage（配置）+ IndexedDB（封面/历史）+ 文件系统（缓存） |
| **实时通信** | Electron IPC（主进程 ↔ 渲染进程 ↔ 桌面歌词窗口） |

---

## 🚀 快速开始

```bash
# 克隆项目
git clone https://github.com/TT-03-KING/Sylara.git

# 安装依赖
npm install

# 启动开发模式
npm start

# 打包 Windows 安装包
npm run dist
