# App Dev Workflow

> 通用 App 開發工作鏈 — 從商業模式到上線，7 階段全流程模板。
> 適合 Flutter / React / Vue / SwiftUI / HTML 任何 App。

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## 這是什麼？

`app-dev-workflow` 是一個給 AI Agent（Hermes、Claude Code、OpenCode 等）使用的 Skill。載入後會自動引導你走完 App 開發的 7 個階段，每一步都有明確的交付物、對應的 AI Skills，和完成檢查點。**Phase 0 的商業模式庫全部來自 5 個真實上線 App 的實戰經驗。**

## 7 階段工作鏈

```
💰 Phase 0: 商業模式 ─→ 6種定價模式 × 11種粘性機制 × 5個真實App數據
📋 Phase 1: 策略     ─→ JTBD + 競品 + MVP 範圍
🎨 Phase 2: 設計     ─→ Design System + 組件庫
🏗️ Phase 3: 架構     ─→ 技術棧 + 目錄結構
🔨 Phase 4: 構建     ─→ 逐功能 TDD 開發
✨ Phase 5: 打磨     ─→ 視覺 QA + 效能
🚀 Phase 6: 上線     ─→ 測試 + 安全 + 發布
```

## 五大真實 App 商業模式

| App | 類型 | 定價 | 粘性機制 |
|-----|------|------|---------|
| **Posture AI** | AI 姿勢矯正 | HK$10/月 | 百日火苗 Streak · 脊椎年齡指標 |
| **Micro-Log** | 語音健康日誌 | HK$10/月 (3次免費) | AI 煉金術動效 · 數字保險庫鎖定 |
| **Oasis Mind** | AI 心理陪伴 | Pro HK$58/月 + 心靈點數制 | 心靈植物養成 · 首次驚喜獎勵 |
| **VIM** | 健身競賽 | HK$58/月 + 積分經濟系統 | 沙盒挑戰賽 · 排行榜競技 |
| **Medic Agent** | 醫療健康平台 | 銀58-鑽石388 (分級 VIP) | 人頭制共享 · 病歷數據累積 |

## 特色

- 💰 **Phase 0 商業模式設計**：6 種定價模式（低價微訂閱、中價會員、分級 VIP、虛擬貨幣/點數制、積分經濟、Freemium）
- 🔥 **11 種用戶粘性機制**：遊戲化進度（Streak/指標/養成）、數據鎖定（保險庫/匯出/歷史）、驚喜時刻（AI動效/個性化/首次獎勵）、信任建立（隱私/本地AI）
- 📈 **含收入預測速算**：轉換率基準、ARPU 基準、盈虧平衡點
- 🎯 **JTBD 驅動**：不猜功能，從用戶真實需求反向推導
- 🧪 **TDD 強制**：每個功能先寫測試再寫代碼

## 源於實戰

這個 Skill 不是理論推導的——所有商業模式和粘性機制都來自 Jeremy Chum 團隊真實開發的 5 個 App：

- **Oasis Mind**：AI 心理陪伴（心靈植物 + 點數經濟）
- **VIM**：健身競賽平台（積分經濟 + 沙盒挑戰 + AI 反作弊裁判）
- **Medic Agent**：醫療健康平台（分級 VIP 人頭制 + 疾病管理）
- **Posture AI**：姿勢矯正（Streak 遊戲化 + 本地 AI 信任）
- **Micro-Log**：語音日誌（AI 煉金術 + 數字保險庫鎖定）

## 安裝

### Hermes Agent

```bash
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
cp template-workflow_state.md /path/to/your-project/.workflow_state.md
```

編輯 `.workflow_state.md` 填入專案名稱，從 Phase 0 開始。

## 適用場景

- 🆕 從零開始做一個新 App
- 🔄 重構/重新設計現有 App
- 📱 Flutter / React Native / SwiftUI 移動端
- 🌐 React / Vue / Next.js Web 端
- 📄 純 HTML 原型 / MVP

## License

MIT — 自由使用、修改、分發。

---

*Made with ❤️ by Jeremy Chum — 5 個真實 App 的開發方法論濃縮*
