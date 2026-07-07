# App Dev Workflow

> 通用 App 開發工作鏈 — 從商業模式到上線，7 階段全流程模板。
> 適用於 Flutter / React / Vue / SwiftUI / HTML 任何 App。

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## 這是什麼？

`app-dev-workflow` 是一個給 AI Agent（Hermes、Claude Code、OpenCode 等）使用的 Skill。載入後會自動引導你走完 App 開發的 7 個階段，每一步都有明確的交付物、對應的 AI Skills，和完成檢查點。

## 7 階段工作鏈

```
💰 Phase 0: 商業模式 ─→ 定價 + 粘性 + 收入預測
📋 Phase 1: 策略     ─→ JTBD + 競品 + MVP 範圍
🎨 Phase 2: 設計     ─→ Design System + 組件庫
🏗️ Phase 3: 架構     ─→ 技術棧 + 目錄結構
🔨 Phase 4: 構建     ─→ 逐功能 TDD 開發
✨ Phase 5: 打磨     ─→ 視覺 QA + 效能
🚀 Phase 6: 上線     ─→ 測試 + 安全 + 發布
```

## 特色

- 💰 **Phase 0 商業模式設計**：4 種定價模式 + 6 種用戶粘性機制（來自真實上線 App 的實戰經驗）
- 🔥 **遊戲化留存**：百日火苗 Streak、脊椎年齡指標、數字保險庫鎖定
- ✨ **驚喜時刻**：AI 煉金術粒子動效、個性化偽定制
- 🎯 **JTBD 驅動**：不猜功能，從用戶真實需求反向推導
- 🧪 **TDD 強制**：每個功能先寫測試再寫代碼

## 安裝

### Hermes Agent

```bash
# 直接複製到 skills 目錄
git clone https://github.com/jeremychum1030/app-dev-workflow.git ~/.hermes/skills/app-dev-workflow
```

或在 Hermes 對話中載入：
```
/skill app-dev-workflow
```

### Claude Code / OpenCode

將 `SKILL.md` 放到專案的 `.claude/skills/` 或 skills 目錄中。

## 使用方法

| 指令 | 效果 |
|------|------|
| `/skill app-dev-workflow` | 顯示當前進度 + 下一步 |
| 「繼續開發」 | 載入當前 Phase 的相關 Skills |
| 「審查設計」 | 觸發設計審查迴圈 |
| 「下一階段」 | 標記完成，推進到下一 Phase |
| 「進度」 | 顯示完整進度總覽 |

## 在專案中使用

```bash
# 複製進度追蹤模板到你的專案
cp template-workflow_state.md /path/to/your-project/.workflow_state.md
```

編輯 `.workflow_state.md` 填入你的專案名稱，然後開始 Phase 0。

## 來自真實專案的商業模式庫

| App | 定價模式 | 核心粘性機制 |
|-----|---------|-------------|
| **Posture AI** | HK$10/月 | 百日火苗 Streak + 脊椎年齡指標 |
| **Micro-Log** | 3次免費→HK$10/月 | AI 煉金術 + 數字保險庫鎖定 |
| **Medic Agent** | HK$58-388 分級 VIP | 人頭制共享 + 數據累積價值 |

## 適用場景

- 🆕 從零開始做一個新 App
- 🔄 重構/重新設計現有 App
- 📱 Flutter / React Native / SwiftUI 移動端
- 🌐 React / Vue / Next.js Web 端
- 📄 純 HTML 原型 / MVP

## License

MIT — 自由使用、修改、分發。

---

*Made with ❤️ by Jeremy Chum — 從真實專案中提取的開發方法論*
