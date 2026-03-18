# TOOLS.md - Local Notes

Skills define _how_ tools work. This file is for _your_ specifics — the stuff that's unique to your setup.

## MissionGet 项目
- **设计规范**: `MEMORY.md` (每次会话自动加载)
- **UI参考**: 风格统一，所有页面位于 workspace 根目录

## 界面文件

| 页面 | 文件名 |
|------|--------|
| 任务大厅 | `bounty-board-apple.html` |
| 角色面板 | `character.html` |
| 任务详情 | `mission-detail.html` |
| 排行榜 | `leaderboard.html` |
| 设置 | `settings.html` |
| 商城 | `shop.html` |
| 每日签到 | `checkin.html` |

## 截图方法（重要！）

**使用 Puppeteer + Edge 无头浏览器截图**，不是 PowerShell GDI（那个只能截可视窗口）

### 脚本位置
`missionget-mvp/frontend/capture-screenshots.js` — 批量截14个页面
`missionget-mvp/frontend/capture-wallet-full.js` — 截单个完整页面

### 使用方法
```bash
# 截全部页面（只截可视窗口）
node missionget-mvp/frontend/capture-screenshots.js

# 截完整页面（滚动截取）
node missionget-mvp/frontend/capture-wallet-full.js
```

### 截图保存位置
`missionget-mvp/frontend/screenshots/`

### 注意事项
- `fullPage: false` = 只截可视窗口
- `fullPage: true` = 截完整页面（可滚动）
- Edge 路径：`C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe`
- 超时时间：30秒
- 截图尺寸：1280×800

## 现有文件

Things like:

- Camera names and locations
- SSH hosts and aliases
- Preferred voices for TTS
- Speaker/room names
- Device nicknames
- Anything environment-specific

## Examples

```markdown
### Cameras

- living-room → Main area, 180° wide angle
- front-door → Entrance, motion-triggered

### SSH

- home-server → 192.168.1.100, user: admin

### TTS

- Preferred voice: "Nova" (warm, slightly British)
- Default speaker: Kitchen HomePod
```

## Why Separate?

Skills are shared. Your setup is yours. Keeping them apart means you can update skills without losing your notes, and share skills without leaking your infrastructure.

---

Add whatever helps you do your job. This is your cheat sheet.
