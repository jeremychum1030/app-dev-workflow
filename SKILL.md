---
name: app-dev-workflow
description: 通用 App 開發工作鏈模板 — 從商業模式到上線的全流程。載入後自動引導當前階段，含來自 Medic Agent/Posture AI/Micro-Log 的真實商業模式庫。
version: 2.0.0
---

# App 開發工作鏈 v2

> `/skill app-dev-workflow` → 顯示當前進度 + 下一步行動
> 適用: Flutter / React / Vue / SwiftUI / HTML 任何 App

---

## 7 階段總覽

```
💰 Phase 0: 商業模式  📋 Phase 1: 策略     🎨 Phase 2: 設計
     ↓                     ↓                     ↓
 定價模型選擇          用戶 Jobs 地圖      Design System
 收入預測              競品分析矩陣        品牌語言
 用戶粘性設計          MVP 範圍定義        組件庫
     ↓                     ↓                     ↓
===================================================
🏗️ Phase 3: 架構     🔨 Phase 4: 構建     ✨ Phase 5: 打磨
     ↓                     ↓                     ↓
技術棧選定            逐功能 TDD 開發       視覺 QA
架構模式              代碼+設計審查迴圈      無障礙+效能
資料流設計                                   
     ↓                     ↓                     ↓
===================================================
🚀 Phase 6: 上線
     ↓
測試+安全+發布
```

---

## Phase 0: 商業模式與營收設計 ⭐ NEW

> **先想清楚怎麼賺錢，再開始寫代碼。**

### 自動載入 Skills
`thinking-inversion` `thinking-first-principles`

### 定價模式庫（來自真實專案）

#### 模式 A: 低價訂閱（Micro-Log / Posture AI）
```
價格: HK$8-15/月
試用: 3次免費 → 付費解鎖
適合: 工具型 App、高頻使用
心理: 「每日不到 0.3 元」降低決策門檻
```

#### 模式 B: 分級 VIP（Medic Agent）
```
銀 HK$58/月  → 僅本人
金 HK$108/月 → 共享 2 人（人均 HK$54）
白金 HK$208/月 → 共享 3 人（人均 HK$69）
鑽石 HK$388/月 → 共享 6 人（人均 HK$65）
關鍵: 人頭制，非人均制 → 鼓勵拉人
```

#### 模式 C: Freemium + 一次性解鎖
```
免費核心功能 → HK$XX 永久解鎖 Pro
適合: 一次性工具、計算器類
```

#### 模式 D: 企業 B2B
```
按席位定價 / 年度合約
適合: B2B SaaS、團隊工具
```

### 用戶粘性設計工具箱

#### 🔥 遊戲化進度
```
- 連續天數計數器 (Streak Counter)
  → Posture AI 的「百日火苗 Day 17」
  → 每日登入/使用 = 火苗持續燃燒
- 個人化指標 (Aspirational Metric)
  → Posture AI 的「脊椎年齡 22 歲（比實際年輕 13 歲）」
  → 給用戶一個想改善的數字
- 進度條 + 成就徽章
  → 「今日處方進度 2/3」
  → 完成 → 火苗值 +N
```

#### 🔒 數據鎖定 (Data Lock-in)
```
- 數字保險庫
  → Micro-Log 的「🏦 個人智慧醫學保險庫」
  → 「永久封存加密您的專屬健康大數據」
  → 用戶累積越多數據，越離不開
- 匯出價值
  → 「AI 自動整理 30 天口述日誌，可直接出示門診」
  → 給用戶看得見的產出（PDF 報告）
```

#### ✨ 驚喜時刻 (Delight Moments)
```
- AI 魔法動效
  → Micro-Log 的「AI 煉金術」粒子爆散動畫
  → 語音輸入後 50 個金/橙色粒子飛出 → 結構化結果出現
  → 讓等待變成期待
- 個性化回饋
  → 「本機 AI 根據今日體態數據·為您深度調配」
  → 偽定制感 = 低成本高感知價值
```

#### 🛡️ 信任建立
```
- 隱私優先定位
  → 「100% 地端 AI 運算 · 影像永不儲存」
  → 「符合 GDPR / HIPAA 標準」
- 本地 AI 標籤
  → 「⬡ Medcore Local AI Core」
  → 強化安全感
```

### 收入預測速算表
```
月收入 = 付費用戶數 × ARPU
付費用戶數 = 總用戶 × 轉換率
轉換率: 免費 App 通常 2-5%
ARPU: 訂閱價 × (1 - 平台抽成 15-30%)

例: 10,000 用戶 × 3% 轉換 × HK$10/月 × 0.85 = HK$2,550/月
```

### 交付物
- [ ] 定價模式選定
- [ ] 3 個用戶粘性機制設計
- [ ] 收入預測速算
- [ ] 付費牆位置設計（哪個功能觸發付費？）

✅ **完成條件:** 商業模式清晰 → Phase 1

---

## Phase 1: 策略 → 「為誰做？解決什麼？不做什麼？」

**載入 Skills:** `thinking-first-principles` `thinking-jobs-to-be-done` `steve-jobs-perspective` `thinking-inversion`

**交付物:**
- [ ] JTBD 用戶工作地圖（5 個核心 Jobs）
- [ ] MVP 功能清單（最多 8 個屏幕/頁面）
- [ ] 不做清單
- [ ] 競品差異化矩陣

✅ **完成條件:** MVP 範圍鎖定 → Phase 2

---

## Phase 2: 設計 → Design System + 組件庫

**載入 Skills:** `design-system` `design-taste-frontend` `brandkit` `minimalist-ui` `high-end-visual-design` `loop-design-check`

**設計 Token 模板:**
```
品牌色: #XXXXXX | 背景: #FFFFFF | 卡片: #F5F7FA
字體: Inter | 字級: 大標24/標題18/正文15/輔文13/小字11
圓角: 卡片12px/按鈕8px | 間距: 屏幕16px/元素12px/區塊24px
```

**核心組件:** Card / Chip / Button / Input / Banner / Accordion / BottomNav / EmptyState

**交付物:**
- [ ] Design Token 文件
- [ ] 8 個核心組件
- [ ] 主頁原型

✅ **完成條件:** 組件庫 + 原型完成 → Phase 3

---

## Phase 3: 架構 → 技術棧 + 目錄結構

**載入 Skills:** `dart-flutter-patterns` / `react-patterns` / `swiftui-patterns`（選對應框架）

**架構決策模板:**
```yaml
框架: Flutter/React/Vue/SwiftUI
狀態管理: Provider/Riverpod/Redux/Zustand
路由: GoRouter/React Router
資料層: Service → Repository → Model
主題: 全局 ThemeData 統一管理
```

**交付物:**
- [ ] 技術棧選定
- [ ] 架構模式確定
- [ ] 目錄結構建立
- [ ] 資料模型定義

✅ **完成條件:** 架構搭建完成 → Phase 4

---

## Phase 4: 構建 → 逐功能 TDD 開發

**載入 Skills:** `orch-build-mvp` `tdd-workflow` `loop-design-check` + 框架 code review skill

**構建順序:** 🔴P0（必須）→ 🟡P1（核心）→ 🟢P2（錦上添花）

**每個功能的閉環:**
```
測試(TDD) → Model → Service → Provider → Screen → 設計審查 → 代碼審查 → ✅
```

**交付物:**
- [ ] P0-1: _______
- [ ] P0-2: _______
- [ ] P1-1: _______
- [ ] P1-2: _______
- [ ] P2-1: _______

✅ **完成條件:** P0+P1 完成 → Phase 5

---

## Phase 5: 打磨 → 視覺 QA + 效能

**載入 Skills:** `high-end-visual-design` `frontend-a11y` `thinking-pre-mortem`

**檢查清單:**
- [ ] 視覺一致：間距/字級/顏色統一
- [ ] 無 overflow：所有文字正常顯示
- [ ] TextScaler 1.2x 測試
- [ ] 無障礙：對比度/標籤
- [ ] 空狀態/錯誤狀態/Loading 狀態齊全
- [ ] 首頁載入 < 1 秒
- [ ] 驚喜時刻動效流暢（如有）

✅ **完成條件:** 所有檢查通過 → Phase 6

---

## Phase 6: 上線 → 測試 + 安全 + 發布

**載入 Skills:** `security-review` `production-audit`

**檢查清單:**
- [ ] 單元/Widget/E2E 測試通過
- [ ] API 密鑰安全檢查
- [ ] 隱私政策 + 權限說明
- [ ] App Store 截圖 + 描述 + 關鍵詞
- [ ] 崩潰監控 + 用戶行為分析接入
- [ ] 付費系統測試（Sandbox 完整走通）

✅ **完成條件:** 正式上架

---

## 使用方法

| 指令 | 效果 |
|------|------|
| `/skill app-dev-workflow` | 顯示進度 + 下一步 |
| 「繼續開發」 | 載入當前 Phase Skills |
| 「審查設計」 | `loop-design-check` |
| 「下一階段」 | 標記完成，下一 Phase |
| 「進度」 | 完整進度總覽 |

## Jeremy 通用規則

- PPT 白底強制，暗色禁止
- UI 不加背景色，透明
- 折疊式佈局優先
- 返回鍵統一左上角
- 繼續=直接執行不總結
- 不追問 bug，自己查
- replace_all 禁用 >500 行

## 來自真實專案的商業模式速查

| 模式 | 定價 | 試用 | 來源 |
|------|------|------|------|
| 低價訂閱 | HK$10/月 | 3次免費 | Posture AI / Micro-Log |
| 分級 VIP | HK$58-388 | 永久免費基礎版 | Medic Agent |
| 數字保險庫 | 付費解鎖 | 有限儲存 | Micro-Log |
| 遊戲化 streak | 免費功能 | N/A | Posture AI |

| 粘性機制 | 心理原理 | 來源 |
|----------|---------|------|
| 百日火苗 | 連續不中斷的承諾 | Posture AI |
| 脊椎年齡 | 個人化進步指標 | Posture AI |
| AI 煉金術 | 等待=期待的魔法時刻 | Micro-Log |
| 保險庫鎖定 | 數據越多越離不開 | Micro-Log |
| 門診報告 | 看得見的產出價值 | Micro-Log |
| 本地 AI 標籤 | 隱私=信任 | Posture AI / Micro-Log |
